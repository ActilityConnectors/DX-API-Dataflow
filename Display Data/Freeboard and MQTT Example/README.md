# Freeboard and MQTT Example
In this tutorial it will be explained how to display device data using a free IoT dashboard called Freeboard.

Freeboard is a simple web panel that shows the information of the different IoT devices that you have connected in real time. And, can fully function in the browser as a static web application without needing a server, acting as a MQTT client. 

In this tutorial Freeboard it is going to be used as a MQTT client connected to a generic MQTT broker.

### Prerequisites to display data in Freeboard:

- ThingPark Wireless application in one of the following network servers: Dev1, IoT, POC.

- Device and Gateway registered in Actility ThingPark Wireless application.

- MQTT broker connected with Actility ThingPark Wireless through a dataflow and AS routing profile previously created.

### Freeboard configuration:

- Create a free trial account in https://freeboard.io/.

- Log in and create a new dashboard in https://freeboard.io/account/.
 
![freeboard dashboard](https://user-images.githubusercontent.com/41436968/43262327-06ab794c-90e0-11e8-95b0-78ea14ca6f07.jpg)

- Create a “datasource” inside your new dashboard and select the protocol or network server from where you want to retrieve the device information. In this case will be MQTT protocol.
 
![freeboard datasource](https://user-images.githubusercontent.com/41436968/43262334-0cb1f08c-90e0-11e8-83cd-542106552632.jpg)
 
![freeboard mqtt](https://user-images.githubusercontent.com/41436968/43262341-13433d66-90e0-11e8-850d-360d84c85413.jpg)

- Put the information of your MQTT broker which will send your device information to Freeboard.
 
![freeboard template example](https://user-images.githubusercontent.com/41436968/43262358-244ef9a6-90e0-11e8-86b4-e920e999b382.png)

Now your connection to Freeboard is ready and you could choose the widget that fit the most to your data!

## Freeboard example with CloudMQTT

In the next figure you will find an example of the information that is need in Freeboard to connect with CloudMQTT following the previous explanation and taking the information of the MQTT example created in the DX-API Dataflow Swagger UI tutorial. 

<p align="center">
  <a href="https://github.com/ActilityConnectors/DX-API-Dataflow/tree/master/Connect%20with%20ThingPark%20Wireless/DX-API%20Dataflow%20Swagger%20UI/MQTT%20Example">CloudMQTT Example</a> 
</p>

Also, don’t forget to create a new user and password for the Freeboard connection in CloudMQTT. Then retrieve the information needed from CloudMQTT: Server URL, port protocol, port name and new user credentials (Name and password).

With the information from your MQTT broker follow the same steps explained above: 
- Go to the Datasource creation in the right corner of Freeboard
- Click "add"
- Put the information needed, take as an example the information displayed in the next figure
 
![freeboard cloudmqtt](https://user-images.githubusercontent.com/41436968/43262363-29b746dc-90e0-11e8-846a-46e186fb2ccd.jpg)

After following these steps, you will have connected Freeboard with CloudMQTT and you are ready to display the device decoded data!
