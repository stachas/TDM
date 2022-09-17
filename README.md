# TDM
Tasmota Device Manager in Docker Container

autodiscovery of Tasmota devices (even if they use custom FullTopics)
module, GPIO and template configuration
rules editor with Var/Mem/Ruletimer monitor
easy to read detachable telemetry viewers (working in active and passive mode)
relay, color and PWM control
user-friendly configuration of buttons, switches and relays, including their related SetOptions
timers editor
clear retained relay and LWT topics
detachable device consoles with command completion and intuitive history
selectable views to see the most vital device parameters at a glance
BSSID aliasing for larger deployments
support for current and legacy Timers payloads (thanks @GrahamM)

Minimum fully-supported Tasmota firmware version: 6.6.0.17

You can also use a VNC client directly at port 5910

Warning:
TDMDock container SHOULD NOT be left running all the time. It does put extra load on the little ESP chips in the Tasmota Devices and on some, it will cause ghost switching and device reboots. It is best to load the container, do your business, then when you are done stop the container. The Terminal window that pops up while the container is running is for troubleshooting and to remind you that the container is running, helping you remember to turn it off when done using the container.



dockerfile
---------------------------------------------------------------------------------------------------
FROM jlesage/baseimage-gui:debian-10

RUN ln -s /usr/lib/x86_64-linux-gnu/libxcb-util.so.0.0.0 /usr/lib/x86_64-linux-gnu/libxcb-util.so.1

RUN apt-get update && apt-get upgrade -y
RUN apt-get install firefox-esr apt-utils -y
RUN add-pkg libqt5x11extras5 python3 python3-pip git -y --no-install-recommends
RUN python3 -m pip install --upgrade pip
RUN python3 -m pip install wheel
RUN python3 -m pip install pyqt5
RUN python3 -m pip install setuptools
RUN python3 -m pip install paho-mqtt

# Install Tasmota Device Manager
RUN pip3 install tdmgr

# Set the name of the application (this appears in the browser)
ENV APP_NAME="Tasmota Device Manager"

# Environment Variables
# see https://github.com/jlesage/docker-baseimage-gui/#environment-variables
ENV TZ="UTC"

# Copy the start script
COPY startapp.sh /startapp.sh

# Create volume
VOLUME /config
---------------------------------------------------------------------------------------------------

startapp.sh
---------------------------------------------------------------------------------------------------
#!/bin/sh
export HOME=/config
export BROWSER=/usr/bin/firefox-esr
exec /usr/bin/python3 /usr/local/bin/tdmgr.py
---------------------------------------------------------------------------------------------------


https://github.com/SirGoodenough/TDMDock
https://zorruno.com/w/TDMDocker
https://github.com/jlesage/docker-baseimage-gui
https://github.com/jziolkowski/tdm
https://github.com/arendst/Tasmota
https://tasmota.github.io/docs/