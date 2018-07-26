# DX-API Dataflow Swagger UI

To create a dataflow, you need to know that each dataflow has its own parameters that you will write down in the DX-API user interface in a JSON or XML format and will create your Dataflow automatically.

Example of an AzureIoT connector

You could know the different parameters for each connector going to the DX-API documentation or using the ThingPark DX-API application (Swagger UI).

For use the documentation go to:

<p align="center">
  <a href="https://dx-api.thingpark.com/dataflow/latest/product/connectors.html">DX-API Dataflow Documentation</a> 
</p>

For use the DX-API Dataflow application click on the Swagger UI button:
 
![get started page](https://user-images.githubusercontent.com/41436968/43263823-ae9ec74a-90e4-11e8-8752-a70c172d1628.png)

And click “Try out!” in the /connectorClasses GET request. Here you will find the different connectors with all the information of each parameter.

As you may see in the documentation or in the application for each connector there are different parameters that you could use putting them in JSON or XML format. For help subscribers here you will find examples codes with the mandatory information for three Dataflow connectors in JSON format. Remember that these connectors could have more parameters that you could find in the documentation.

Code HTTP connector

Code MQTT connector

Code AzureIoTHub connector

Now with this examples codes you can change the required information and follow the next steps:

- Go to the DX API Dataflow
- Select the POST /bridgeDataflows request
- Paste your code in the Value box as it shows Figures 4 and 5.
 
![mqtt connector example](https://user-images.githubusercontent.com/41436968/43263824-aeb629a8-90e4-11e8-80ff-d0b3cf917b54.png)
 
![http connector example](https://user-images.githubusercontent.com/41436968/43263825-aecf38bc-90e4-11e8-8629-e83fe92dff8b.png)

- Click the “Try it out!” button
- If you follow all the steps correctly your Dataflow will be waiting for the validation process. When the process is done you will receive the email displayed in Figure 3 with the information of your connector:
 
![email example](https://user-images.githubusercontent.com/41436968/43263826-aee912e6-90e4-11e8-8cde-077300be4436.png)

After you receive this email now you can go to the Actility ThingPark interface or to the DX Core API and create a new routing profile that points to the next URL:

<p align="center"> https://dx-api.thingpark.com/dataflow/latest/api/uplinkMessages </p>

And your Dataflow will be ready and sending your device information every time that your device sends information to the Actility Network.
