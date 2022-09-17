# TDM
Tasmota Device Manager in Docker Container

- autodiscovery of Tasmota devices (even if they use custom FullTopics)
- module, GPIO and template configuration
- rules editor with Var/Mem/Ruletimer monitor
- easy to read detachable telemetry viewers (working in active and passive mode)
- relay, color and PWM control
- user-friendly configuration of buttons, switches and relays, including their related SetOptions
- timers editor
- clear retained relay and LWT topics
- detachable device consoles with command completion and intuitive history
- selectable views to see the most vital device parameters at a glance
- BSSID aliasing for larger deployments
- support for current and legacy Timers payloads (thanks @GrahamM)

Minimum fully-supported Tasmota firmware version: 6.6.0.17

You can also use a VNC client directly at port 5910

Warning:
TDMDock container SHOULD NOT be left running all the time. It does put extra load on the little ESP chips in the Tasmota Devices and on some, it will cause ghost switching and device reboots. It is best to load the container, do your business, then when you are done stop the container. The Terminal window that pops up while the container is running is for troubleshooting and to remind you that the container is running, helping you remember to turn it off when done using the container.

To create the Docker will take a little time. 
Image will be big with 1.2 GB

I use a MQTT Broker on another Server!

<img width="973" alt="image" src="https://user-images.githubusercontent.com/113388310/190870976-0685a2bc-1eaf-4137-969c-1c24308129cf.png">

<img width="272" alt="image" src="https://user-images.githubusercontent.com/113388310/190870997-c65c4c3b-d128-43ea-8a96-5fc165ada1e7.png">

<img width="188" alt="image" src="https://user-images.githubusercontent.com/113388310/190871022-3942f449-8d33-4af4-8612-6f144af5799f.png">

<img width="226" alt="image" src="https://user-images.githubusercontent.com/113388310/190871059-bee20cb6-9b67-43ef-9406-6a8b296eb948.png">

<img width="159" alt="image" src="https://user-images.githubusercontent.com/113388310/190871119-151d5bf1-83c2-49ea-abe3-dc7034219c16.png">

<img width="202" alt="image" src="https://user-images.githubusercontent.com/113388310/190871130-b33c1922-e9be-4665-84b3-eee4788e3a8f.png">

<img width="167" alt="image" src="https://user-images.githubusercontent.com/113388310/190871141-4e09b2da-a104-4dab-81a3-9d326c86da91.png">

<img width="961" alt="image" src="https://user-images.githubusercontent.com/113388310/190871161-e6b83a9e-f063-40bc-a5cd-78befbb6ba2f.png">




My thanks go to:

https://github.com/SirGoodenough/TDMDock

https://zorruno.com/w/TDMDocker

https://github.com/jlesage/docker-baseimage-gui

https://github.com/jziolkowski/tdm

https://github.com/arendst/Tasmota

https://tasmota.github.io/docs/

