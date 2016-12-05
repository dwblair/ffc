# 12-5-2016

Following Atomiton instructions ...

- Gateway and sensor hub connected.  Soil moisture measurements being logged.

<img src="assets/12_5_2016_sensor_hub_001.png" width=500>

<img src="assets/12_5_2016_sensor_hub_002.png" width=500>

<img src="assets/12_5_2016_sensor_hub_moisture_drop_003.png" width=500>

<img src="assets/12_5_2016_sensor_hub_moisture_long_decay_while_wetting_004.png" width=500>

<img src="assets/12_5_2016_sensor_hub_moisture_recovery_while_drying_005.png" width=100%>

Don't currently have router to connect to etherport from gateway.  Will look into finding router.


Sensor ... 

http://192.168.0.1:8080/fid-smartfarmui/app/index.html#/zone/SampleZone

Alfalfa-SensorHub - fc:db:b3:ac:da:5c


http://target.atomiton.com:8080/fid-dashboard/app/index.html

select second "SampleZone" from drop-down menu

soil moisture probe:

irrometer -- watermark -- http://irrometer.com/pdf/sensors/403%20WATERMARK%20Sensor-WEB.pdf

https://www.cooking-hacks.com/documentation/tutorials/how-to-measure-soil-moisture-humidity-and-temperature-using-waspmote/

suggestion for calibration -- "How can I check the sensors?" -- suggests submerging in water

http://www.irrometer.com/faq.html

-----

# LORA

This is the model we have:

http://www.multitech.com/models/94557148LF

- [manual](http://www.multitech.com/documents/publications/manuals/s000612.pdf)


- dmesg after plugging in:

scsi 2:0:0:0: Direct-Access     MBED     microcontroller  1.0  PQ: 0 ANSI: 2
[23622.850389] sd 2:0:0:0: Attached scsi generic sg1 type 0
[23622.853387] sd 2:0:0:0: [sdb] 1056 512-byte logical blocks: (541 kB/528 KiB)
[23622.855960] sd 2:0:0:0: [sdb] Write Protect is off
[23622.855968] sd 2:0:0:0: [sdb] Mode Sense: 03 00 00 00

Set the following:
■ Baud rate = 115,200
■ Data bits = 8
■ Parity = N
■ Stop bits = 1
■ Flow control = Off

sudo screen /dev/ttyACM1 115200

Can talk to device -- got:

AT

OK

mdot documentation:

https://developer.mbed.org/platforms/MTS-mDot-F411/

mbed library:

https://github.com/armmbed/mbed-os

----

atomiton setup

https://atomiton.atlassian.net/wiki/display/TQLDocs/TQL+and+IoT+application+topology

----

installing multitech lorawan conduit -- things network

https://www.thethingsnetwork.org/wiki/LoRaWAN/Overview


Following instructions here:

things network -- setting up the multiconnect conduit:

https://www.thethingsnetwork.org/docs/current/multitech/

--- looks like i'll need an ethernet connection -- maybe a USB - ethernet dongle 

-- got one

multitech first time setup wizard

username: admin
password: ffc

----

First, how does the TQL sensor hub connect to the TQL gateway?  this is how we'll connect the multitech to the TQL gateway ...

Documentation for TQL System:

https://atomiton.atlassian.net/wiki/display/TQLDocs/TQL+Docs

atomiton agrikit docs:

https://atomiton.atlassian.net/wiki/display/TQLDocs/Agriculture+Dev+Kit?preview=/44368015/44368014/AtomitonAgriKit-1Pager.pdf

adding additional sensors to the TQL sensor hub

https://atomiton.atlassian.net/wiki/display/TQLDocs/Adding+Additional+Sensors+to+TQL+Sensor+Hub

----

see under 'gateway setup':

https://atomiton.atlassian.net/wiki/display/TQLDocs/11.+Gateways%2C+Cloud+-+Edge+Computing

installing the TQL engine ...

https://atomiton.atlassian.net/wiki/display/TQLDocs/Download+and+install+TQLEngine

console model editor

https://atomiton.atlassian.net/wiki/display/TQLDocs/Console+Model+Editor





 

