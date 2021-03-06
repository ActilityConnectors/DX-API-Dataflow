# Tutorial 2: Display Data
Here it will be shown how to display data using an IoT dashboard, or in other words, a graphical user interface where users can manage their IoT solution for data collection, processing, visualization and device management.

## Freeboard and MQTT Example
In this tutorial it will be explained how to display device data using a free IoT dashboard called Freeboard.

Freeboard is a simple web panel that shows the information of the different IoT devices that you have connected in real time. And, can fully function in the browser as a static web application without needing a server, acting as a MQTT client. 

### Prerequisites to display data in Freeboard:

- ThingPark Wireless application in one of the following network servers: Dev1, IoT, POC.

- Device and Gateway registered in Actility ThingPark Wireless application.

- MQTT broker connected with Actility ThingPark Wireless through a dataflow and AS routing profile previously created. Follow the MQTT tutorial [here](https://github.com/ActilityConnectors/DX-API-Dataflow/tree/master/Display%20Data/MQTT%20Tutorial)!

### Freeboard configuration

- Create a free trial account in https://freeboard.io/.

- Log in and create a new dashboard in https://freeboard.io/account/.

<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43262327-06ab794c-90e0-11e8-95b0-78ea14ca6f07.jpg">
</p>

- Create a “datasource” inside your new dashboard and select the protocol or network server from where you want to retrieve the device information. In this case will be MQTT protocol.

<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43262334-0cb1f08c-90e0-11e8-83cd-542106552632.jpg">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43262341-13433d66-90e0-11e8-850d-360d84c85413.jpg">
</p>

- Put the information of your MQTT broker which will send your device information to Freeboard.
 
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43262358-244ef9a6-90e0-11e8-86b4-e920e999b382.png">
</p>

- See the next image as a real example of the information requeried by freeboard, taking the information of the [MQTT Connector with CloudMQTT](https://user-images.githubusercontent.com/41436968/43328454-4ddf1150-91be-11e8-9bb2-261c414fe3c5.JPG) tutorial. 
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43262363-29b746dc-90e0-11e8-846a-46e186fb2ccd.jpg">
</p>

- Click "Save" and that's it!

After following these steps, you will have connected Freeboard with CloudMQTT and you are ready to display the device decoded data!

See an example using two gauge widgets in the next image:
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43325221-7043b910-91b6-11e8-8ee1-9f91c5ea1faa.JPG">
</p>
