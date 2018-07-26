# Dataflow Theory

To understand the working architecture of a dataflow, see the next figure. This figure shows the main parts of a Dataflow which is composed by a binder processor, a decoder unit, and a 1-to-N connector. Components that must be defined in the application.

![dx-api dataflow scheme](https://user-images.githubusercontent.com/41436968/43260523-13949d42-90da-11e8-8196-ddb6b9352db6.jpg)

To get started follow the next link, introduce your credentials and you will have access to the DX-API application and documentation:

<p align="center">
  <a href="https://dx-api.thingpark.com/getstarted/#/">Get Started</a>
</p>

Select the “DX Dataflow API Swagger-UI” and follow the next steps to create your Dataflow.

To create a dataflow, you need to know that each dataflow has its own parameters that you will write down in the DX-API user interface in a JSON or XML format and will create your Dataflow automatically.

<p align="center">
  <a href="https://github.com/ActilityConnectors/DX-API-Dataflow/blob/master/Connect%20with%20ThingPark%20Wireless/DX-API%20Dataflow%20Swagger%20UI/Connectors%20Example%20Code/AzureIoTHub%20Connector.json">Example of an AzureIoT connector</a> 
</p>

You could know the different parameters for each connector going to the DX-API documentation or using the ThingPark DX-API application (Swagger UI).

For use the documentation go to:

<p align="center">
  <a href="https://dx-api.thingpark.com/dataflow/latest/product/connectors.html">DX-API Dataflow Documentation</a> 
</p>

For use the DX-API Dataflow application click on the Swagger UI button:

<p align="center">
  <img src="https://user-images.githubusercontent.com/41436968/43263823-ae9ec74a-90e4-11e8-8752-a70c172d1628.png">
</p>

And click “Try out!” in the /connectorClasses GET request. Here you will find the different connectors with all the information of each parameter.
