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





My thanks go to:

https://github.com/SirGoodenough/TDMDock
https://zorruno.com/w/TDMDocker
https://github.com/jlesage/docker-baseimage-gui
https://github.com/jziolkowski/tdm
https://github.com/arendst/Tasmota
https://tasmota.github.io/docs/

