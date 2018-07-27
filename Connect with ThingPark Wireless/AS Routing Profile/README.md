# AS Routing Profile

The AS (Application Server) routing profile defines how the sensor data is routed to an application server.
This is the easiest way to obtain data from Actility, only set a routing profile that point at the HTTP server of your preference, and you will start receiving coded data of the device in form of a POST request in JSON or XML format.

As an example, you could create a simple Generic HTTP Listener following the steps describer in the Actility Git-Hub:

<p align="center">
  https://github.com/actility/generic-http-listener 
</p>                                     

With this HTTP server, you could see how Actility send coded device data and create your own application. But if you don’t want to create your own application right now, and you want to use this feature you can use http://dweet.io/, which give users the opportunity to send messages to a HTTP server and display them in an easy way.

### Actility and Dweet Tutorial
Dweet allows users to send data to a specific URL that follow the next pattern:

<p align="center">
  https://dweet.io/dweet/for/my-thing-name?hello=world
</p>        

Where “my-thing-name” is a unique name of your choice. So, when you have your thing name decided, go to the ThingPark Wireless interface and create a routing profile that points to this new URL.

To achieve this, follow the next steps:
- Enter in your ThingPark Wireless user interface.

- Create a new application server.

- Create a new AS Routing Profile and associate the previous application server created.

- Open your device network settings going to Devices -> List -> Edit (Pencil tool)

- Go to Network settings and associate your new AS Routing Profile

Finally, if you want to retrieve the data just follow the next link, replacing your “thing name” and you will see your device payload.

<p align="center">
  https://dweet.io/get/latest/dweet/for/my-thing-name
</p>  


