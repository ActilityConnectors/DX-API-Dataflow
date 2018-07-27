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
- Enter in your ThingPark Wireless user interface
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43329618-2badfe40-91c1-11e8-8405-d4562fd01ee3.JPG">
</p>

- Create a new application server with the URL given above and your thing name (In this tutorial the application server will be called Dweet and will point to https://dweet.io/dweet/for/ElsysERS?hello=world)
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43329759-a0515364-91c1-11e8-9074-36dd471f25e1.JPG">
</p>

- Create a new AS Routing Profile and associate the previous application server created (In this tutorial the AS Routing Profile will be called Dweet as well)
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43329965-27c549a4-91c2-11e8-883b-6de684be30a5.jpg">
</p>

- Open your device network settings going to Devices -> List -> Edit (Pencil tool)
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43330118-926e1c5e-91c2-11e8-9624-80bfb19d0f3a.JPG">
</p>

- Go to Network settings and associate your new AS Routing Profile
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43330257-f6f57f3c-91c2-11e8-91e9-fb7aaa2f0541.JPG">
</p>

That's it your AS Routing Profile is ready! if you want to retrieve the data just follow the next link, replacing your “thing name” and you will see your device payload.

<p align="center">
  https://dweet.io/get/latest/dweet/for/my-thing-name
</p>  

In the example of this tutorial the information is showed in the next way by Dweet:
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43330526-b9a84ce4-91c3-11e8-8b32-e1570d4d1b2c.JPG">
</p>


