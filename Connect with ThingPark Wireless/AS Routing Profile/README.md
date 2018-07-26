# AS Routing Profile

The AS (Application Server) routing profile defines how the sensor data is routed to an application server.
This is the easiest way to obtain data from Actility, only set a routing profile that point at the HTTP server of your preference, and you will start receiving coded data of the device in form of a POST request in JSON or XML format.

As an example, you could create a simple Generic HTTP Listener following the steps describer in the Actility Git-Hub in the following link:
     
                                          https://github.com/actility/generic-http-listener

With this HTTP server, you could see how Actility send coded device data and create your own application. If you don’t want to create your own application right now, but you want to use this feature you can use dweet.io, which give users the opportunity to send messages to a HTTP server and display them in an easy way.

