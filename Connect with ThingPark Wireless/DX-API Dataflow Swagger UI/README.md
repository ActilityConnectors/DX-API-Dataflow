# DX-API Dataflow Swagger UI

The purpose of this API is to provide the best experience for all developers who want to interface with ThingPark applications to receive and send messages from their IoT devices.

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

Now with this examples codes you can change the required information and follow the next steps:

- Go to the DX API Dataflow
- Select the POST /bridgeDataflows request
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43319554-7a273a08-91a5-11e8-978e-9a1858747290.JPG">
</p>

- Paste your code in the Value box as it shows the next figure.
<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43319735-2003db34-91a6-11e8-920a-f5f93530b6a3.JPG">
</p>

- Click the “Try it out!” button
- If you follow all the steps correctly your Dataflow will be waiting for the validation process. When the process is done you will receive the next email with the information of your connector:
 
![email example](https://user-images.githubusercontent.com/41436968/43263826-aee912e6-90e4-11e8-8cde-077300be4436.png)

While the activation process is completed you can go to the Actility ThingPark interface or to the DX Core API and create a new AS routing profile that points to the next URL:

<p align="center"> https://dx-api.thingpark.com/dataflow/latest/api/uplinkMessages </p>

Set this routing profile in your devices and that's it! Your Dataflow is now ready and sending your device information.
