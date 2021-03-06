# DX-API Dataflow Swagger UI

The purpose of this API is to provide the best experience for developers who want to interface with ThingPark applications to receive and send messages from their IoT devices.

### Link to theory
If you want to familiarize yourself with the functioning of the DX-API Dataflow, do not hesitate and go to the DX-API documentation. Here you could read how this tool works in the front and back end. 
<p align="center">
  <a href="https://dx-api.thingpark.com/dataflow/latest/product/home.html">DX-API Documentation</a> 
</p>
On the other hand, if you know how the Dataflows works or you only want to create a quick proof-of-concept continue through the tutorial!

### DX-API Tutorial
First go to the DX-API Dataflow application following the next link, introduce your credentials and you will have access to all DX-API applications and documentation:

<p align="center">
  <a href="https://dx-api.thingpark.com/getstarted/#/">Get Started</a>
</p>

Select the “DX Dataflow API Swagger-UI” and follow the next steps to create your Dataflow.

<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43272237-c500bbfa-90f9-11e8-8aac-79b854e2a856.png">
</p>

To create a dataflow, you need to know that each dataflow has its own parameters that you need to define and write down in the DX-API Swagger user interface in a JSON or XML format to create it. For each connector there are different parameters that you could use and for assist subscribers in the "Connectors Example Code" and "Connectors Templates" folders you will find examples codes with the only the mandatory information for the Dataflow connectors in JSON format. Remember that these connectors could have more parameters that you could find in the documentation, in other words, in this tutorial and with the example codes it will be shown how to create the most basic connectors.

Now with these examples codes you can change the required information and follow the next steps:

- Go to the DX API Dataflow
- Select the POST /bridgeDataflows request
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43319554-7a273a08-91a5-11e8-978e-9a1858747290.JPG">
</p>

- Create your JSON code, see the next example where it is explained each part of the code in comments (But don’t forget to erase the comments if you are going to use this code, remember that JSON files dosen't support comments!)

```
{
  "id": "",                            // ID of your preference, must have at least 6 characters
  "name": "",                          // Name of your preference
  "bidirectional": false,              // Define the use case of the connector, false = Uplink , true = Uplink and Downlink
  "binder": {
    "classRef": "LRC_HTTP",            // Currently Binder Processor available for dataflows creation (Don't change this)
    "properties": {
      "deviceEUIList": ""              // Your dev EUI key, this device should be registerer in your ThingPark Wireless account
    }
  },
  "driver": {
    "classRef": ""                     // Decoder to be used by the connector, go to https://dx-api.thingpark.com/dataflow/latest/product/drivers.html to see the decoders available
  },
  "connectors": [
    {
      "classRef": "GenericMQTT",       // Reference name of the connector, go to https://dx-api.thingpark.com/dataflow/latest/product/connectors.html to see the connectors available
      "properties": {                  // From this part onwards are the properties of each connector. Go to the connector of your preference in the previous link and choose the properties that fit the most for your cloud connection
        "hostName": "HostServer:Port",  
        "protocol": "",                
        "accountPrefix": "",
        "login": "",
        "password": ""
      }
    }
  ]
}
```

- Paste your code in the Value box as it shows the next image (Taking the [MQTT example](https://github.com/ActilityConnectors/DX-API-Dataflow/blob/master/Connect%20with%20ThingPark%20Wireless/DX-API%20Dataflow%20Swagger%20UI/Connectors%20Templates/MQTT%20Template.json) code, remember that you could use the blank templates and fill them with your information).
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43319735-2003db34-91a6-11e8-920a-f5f93530b6a3.JPG">
</p>

- Click the “Try it out!” button
- If you follow all the steps correctly your Dataflow will be waiting for the validation process. When the process is done you will receive the next email with the information of your connector:
 
![email example](https://user-images.githubusercontent.com/41436968/43263826-aee912e6-90e4-11e8-8cde-077300be4436.png)

While the activation process is completed you can go to the Actility ThingPark interface or to the DX Core API and create a new AS routing profile that points to the next URL:

<p align="center"> https://dx-api.thingpark.com/dataflow/latest/api/uplinkMessages </p>
To achieve this, follow the next steps:

- Enter in your ThingPark Wireless user interface
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43329618-2badfe40-91c1-11e8-8405-d4562fd01ee3.JPG">
</p>

- Create a new HTTP application server with the URL given above (In this tutorial the application server will be called Dataflow, but you can choose the name of your preference)
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43402750-bcba36a2-9413-11e8-99e0-881c53c2ff78.JPG">
</p>

- Create a new AS Routing Profile and associate the previous application server (In this tutorial the AS Routing Profile will be called Dataflow as well)
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43402761-bf00cdea-9413-11e8-9b8f-171a98774046.jpg">
</p>

- Open your device network settings going to Devices -> List -> Edit (Pencil tool)
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43402765-c0a3285a-9413-11e8-86b2-1ce1e255f0b4.JPG">
</p>

- Go to Network settings and associate your new AS Routing Profile
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43402768-c231b7e0-9413-11e8-9e71-bd5e0a17ed0d.jpg">
</p>

That's it your AS Routing Profile is ready! Your Dataflow is now ready and sending your device information. 
If you want to see a more specific tutorial, continue and discover how to create a MQTT connector with CloudMQTT!

## MQTT Connector with CloudMQTT

To create a new MQTT dataflow here will be explained how to connect with a free third party MQTT broker called CloudMQTT.

### Prerequisites:

- ThingPark Wireless application in one of the following network servers: Dev1, IoT, POC.

- Device and Gateway registered in Actility ThingPark Wireless application.

- CloudMQTT account (could be a free or paid account).

### Configuration:

- Create an instance and go to details where you will find your MQTT host and the ports to connect using different protocols, see next image.
 
![cloudmqtt instance](https://user-images.githubusercontent.com/41436968/43262792-a965bcc8-90e1-11e8-844a-cc40fbd41d6a.png)

- Create a user which will be the credentials to connect with Actility with this MQTT Broker.
 
![user credentials](https://user-images.githubusercontent.com/41436968/43262794-ab4031fe-90e1-11e8-822e-973e794b3a70.png)

- Finally, create a topic from where you expect to receive data, you could use a wild card topic using the “#” symbol and give the Read and Write access to the user.

<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43262799-ac8277d4-90e1-11e8-8441-c29f86f70488.png">
</p>

- With this configuration you are ready to create and test a MQTT Dataflow! Save the information obtained in the previous steps: Server URL, port protocol, port number, user name and password.

Now you can go to the DX-API Dataflow application and follow the next steps:

- Select the POST /bridgeDataflows request
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43319554-7a273a08-91a5-11e8-978e-9a1858747290.JPG">
</p>

- Create your JSON/XML code filling the blank spaces in the following text:

```json
{
  "id": "",                            
  "name": "",                          
  "bidirectional": false,             
  "binder": {
    "classRef": "LRC_HTTP",            
    "properties": {
      "deviceEUIList": ""              
    }
  },
  "driver": {
    "classRef": ""                     
  },
  "connectors": [
    {
      "classRef": "GenericMQTT",       
      "properties": {                  
        "hostName": "HostServer:Port",  
        "protocol": "",                
        "accountPrefix": "",
        "login": "",
        "password": ""
      }
    }
  ]
}
```

- Paste your code in the POST /bridgeDataflows request (Here it will be use the blank example code with the infomation previously gathered and one Elsys sensor)
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43328454-4ddf1150-91be-11e8-9bb2-261c414fe3c5.JPG">
</p>

- Click the “Try it out!” button

- Now your connector will be waiting for the validation process. When the process is done you will receive an email with a change of status to READY for your connector

Don’t forget creating your Dataflow AS routing profile that points to the next URL:

<p align="center">
  https://dx-api.thingpark.com/dataflow/latest/api/uplinkMessages
</p>

Set this routing profile (As it is shown above) in your devices and that's it! Your Dataflow is now ready and sending your device information. Go to the WebSocket UI on CloudMQTT to see the messages incoming from Actility.
