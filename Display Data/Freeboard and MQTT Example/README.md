# Freeboard and MQTT Example
You can create your own IoT dashboard or use one of the different solutions available on the internet, in this guide we are going to explain how to display device data using a free IoT dashboard called Freeboard.
Freeboard is a simple web panel that shows the information of the different IoT devices that you have connected in real time. And, can fully function in the browser as a static web application without the need for a server, acting as a MQTT client. In this guide Freeboard it is going to be used as a MQTT client connected to a MQTT broker.
Prerequisites to display your data in Freeboard:
•	ThingPark Wireless application in one of the following network servers: Dev1, IoT, POC.
•	Device and Gateway registered in Actility ThingPark Wireless application.
•	MQTT broker connected with Actility ThingPark Wireless through a dataflow and AS routing profile previously created.

Freeboard configuration:
•	Create a free trial account in https://freeboard.io/.
•	Log in and create a new dashboard in https://freeboard.io/account/.
 
Figure 9. Dashboard Creation
•	Create a “datasource” inside your new dashboard and select the protocol or network server from where you want to retrieve the device information. In this case will be MQTT protocol.
 
Figure 10. Add New DataSource

 
Figure 11. MQTT Selection

•	Put the information of your MQTT broker which will send your device information to Freeboard.
 
Figure 12. Connection with a MQTT Broker
Now your connection to Freeboard is ready and you could choose the widget that fit the most to your data!

Freeboard example with CloudMQTT:
In the Figure 13 you will find an example of the information that is need in Freeboard to connect with CloudMQTT taking the information of the previous CloudMQTT example created. Also, don’t forget to create a new user and password for the Freeboard connection, and retrieve all the information needed from CloudMQTT: Server URL, port and user credentials (Name and password).

With the information from your MQTT broker go to the Datasource creation, click add and put the information displayed in Figure 13. After following these steps, you will have connected Freeboard with CloudMQTT and you are ready to display the device decoded data!

 
Figure 13. Connection with CloudMQTT

