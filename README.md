# DX-API-Dataflow

ThingPark DX-API provides a dataflow management solution to process uplink and downlink data. It allows developers to design and deploy new dataflows for specific sets of subscriber devices, thus enabling data processing on top of the ThingPark Wireless solution for those devices.

Every configured dataflow is executed within a unique dataflow execution instance. That specific instance can then be associated with multiple devices within the scope of a ThingPark subscriber. A dataflow can be bidirectional, meaning an execution instance can receive and process its device’s uplinks, but also process and send downlinks to its devices.

