# MQTT Connector with CloudMQTT

To create a new MQTT dataflow here will be explained how to connect with a free third party MQTT broker called CloudMQTT.

Prerequisites:

- ThingPark Wireless application in one of the following network servers: Dev1, IoT, POC.

- Device and Gateway registered in Actility ThingPark Wireless application.

- CloudMQTT account (could be a free or paid account).

### Configuration:

- Create an instance and go to details where you will find your MQTT host and the ports to connect using different protocols, see Figure 6.
 
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

<p align="center">
  <a href="https://github.com/ActilityConnectors/DX-API-Dataflow/blob/master/Connect%20with%20ThingPark%20Wireless/DX-API%20Dataflow%20Swagger%20UI/Connectors%20Templates/MQTT%20Template.json">CloudMQTT Example</a>
</p>

- Paste your code in the POST /bridgeDataflows request (Here it will be use the blank example code with the infomation previously gathered)
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43320976-bedbb124-91aa-11e8-9854-17493a0a4018.JPG">
</p>

- Click the “Try it out!” button

When you receive the validation email your connector will be ready! Don’t forget creating your Dataflow AS routing profile and then go to the WebSocket UI on CloudMQTT to see the messages incoming from Actility.
