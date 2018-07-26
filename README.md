# DX-API-Dataflow

ThingPark DX-API provides a dataflow management solution to process uplink and downlink data. It allows developers to design and deploy new dataflows for specific sets of subscriber devices, thus enabling data processing on top of the ThingPark Wireless solution for those devices.

Every configured dataflow is executed within a unique dataflow execution instance. That specific instance can then be associated with multiple devices within the scope of a ThingPark subscriber. A dataflow can be bidirectional, meaning an execution instance can receive and process its device’s uplinks, but also process and send downlinks to its devices.

## DX-API Dataflow Swagger UI

The purpose of this API is to provide the best experience for all developers who intend to interface with ThingPark applications to receive and send messages from they IoT devices.
To use the ThingPark DX-API Dataflow application you need to have a ThingPark Developer account in any of the following network servers:

- Dev1
  
- POC
  
- IoT
  
To understand the working architecture of a dataflow, see the Figure 1. This figure shows the main parts of a Dataflow which is composed by a binder processor, a decoder unit, and a 1-to-N connector. Components that must be defined in the application.

![dx-api dataflow scheme](https://user-images.githubusercontent.com/41436968/43260523-13949d42-90da-11e8-8196-ddb6b9352db6.jpg)

To get started follow the next link, introduce your credentials and you will have access to the DX-API application and documentation:

<p align="center">
  <a href="https://dx-api.thingpark.com/getstarted/#/">Get Started</a>
</p>

Select the “DX Dataflow API Swagger-UI” and follow the next steps to create your Dataflow.
