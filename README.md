# Time of Flight Monitor Example

This application demonstrates how can someone use an XPLR-IOT-1 device to get measurement data from a wireless Bluetooth LE sensor, and how can these data be sent to the Thingstream platform via MQTT, and then visualized in a Node-RED dashboard.\
For this purpose a Wireless Time of Flight sensor is implemented. This solution consists of the elements shown in the picture that follows:

- A Bluetooth LE sensor measurement broadcaster (wireless sensor)
- An XPLR-IOT-1 Gateway
- A Thingstream flow which gets the measurements and publishes them to the dashboard
- A Node-RED dashboard for data visualization

![ToFSolution should be here.](readme_images/devices/ToFMonitorSolution.jpg "Time of Flight Monitor Solution")

In this project a wireless Bluetooth LE sensor is implemented using a [AMS TMF8828 sensor](https://ams.com/en/tmf8828) in a [MikroE LightRanger9](https://www.mikroe.com/lightranger-9-click).\
In order to render this sensor wireless you can connect it to a [MINI-NORA-B1 Evaluation kit](https://www.u-blox.com/en/product/mini-nora-b1).

The wireless sensor broadcasts its measurements via Bluetooth LE, and an XPLR-IOT-1 device can be used as a Gateway to pick up those measurements, and send them via a Wi-Fi connection to Thingstream platform using MQTT protocol.

After been transmitted to Thingstream, a Thingstream flow can be created to publish those measurements to a Node-RED dashboard for visualisation.

All these elements are implemented in this project, to provide a complete example.


- The wireless Time of Flight sensor is implemented and described [here](./sensor_broadcaster)
- The Time of Flight Gateway is implemented and described [here](./Gateway)
- The Thingstream flow is described [here](./thingstream_flow)
- The Node-RED dashboard can be found [here](./node-red) 


## Disclaimer
Copyright &copy; u-blox 

u-blox reserves all rights in this deliverable (documentation, software, etc.,\
hereafter “Deliverable”). 

u-blox grants you the right to use, copy, modify and distribute the\
Deliverable provided hereunder for any purpose without fee.

THIS DELIVERABLE IS BEING PROVIDED "AS IS", WITHOUT ANY EXPRESS OR IMPLIED\
WARRANTY. IN PARTICULAR, NEITHER THE AUTHOR NOR U-BLOX MAKES ANY\
REPRESENTATION OR WARRANTY OF ANY KIND CONCERNING THE MERCHANTABILITY OF THIS\
DELIVERABLE OR ITS FITNESS FOR ANY PARTICULAR PURPOSE.

In case you provide us a feedback or make a contribution in the form of a\
further development of the Deliverable (“Contribution”), u-blox will have the\
same rights as granted to you, namely to use, copy, modify and distribute the\
Contribution provided to us for any purpose without fee.