# Actility and CloudMQTT Tutorial

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

Set this routing profile in your devices defined in the dataflow and that's it! Your Dataflow is now ready and sending your device information. Go to the WebSocket UI on CloudMQTT to see the messages incoming from Actility.
