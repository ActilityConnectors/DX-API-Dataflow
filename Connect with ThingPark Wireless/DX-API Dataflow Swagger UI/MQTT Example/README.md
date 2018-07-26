# MQTT Connector with CloudMQTT

To create a new MQTT dataflow here will be explained how to connect with a free third party MQTT broker called CloudMQTT.

Prerequisites:

  •	ThingPark Wireless application in one of the following network servers: Dev1, IoT, POC.

  •	Device and Gateway registered in Actility ThingPark Wireless application.

  •	CloudMQTT account (could be a free or paid account).

Configuration:

  •	Create an instance and go to details where you will find your MQTT host and the ports to connect using different protocols, see Figure 6.
 
Figure 6. CloudMQTT Instance Details.

  •	Create a user which will be the credentials to connect with Actility with this MQTT Broker.
 
Figure 7. User Credentials Creation.

  •	Finally, create a topic from where you expect to receive data, you could use a wild card topic using the “#” symbol and give the Read and Write access to the user.
 
Figure 8. User Topic and Permits Creation.

  •	With this configuration you are ready to create and test a MQTT Dataflow! Save the information obtained in the previous steps: Server URL, port protocol and number, user name and password.

With your CloudMQTT account you can go to the DX-API Dataflow application and follow the next steps:
  •	Select the POST /bridgeDataflows request

  •	Create your JSON/XML code filling the blank spaces in the following text:

CloudMQTT Example

  •	Paste your code in the POST /bridgeDataflows request

  •	Click the “Try it out!” button

When you receive the validation email your connector will be ready! Don’t forget creating your Dataflow AS routing profile and then go to the WebSocket UI on CloudMQTT to see the messages incoming from Actility.
