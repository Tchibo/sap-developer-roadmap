The enterprise event enablement provides the ability to exchange events between SAP S/4HANA and a message broker. It supports outbound / publish as well as inbound/ subscribe scenarios.

In order to either publish or consume events its necessary to define a channel to a message broker. Via outbound binding all event topics are defined that shall be published on this channel to the message broker. The inbound binding works in the same way with subscribing to a queue on the broker and to a certain event topic coming from this queue.

The configuration of the channels is done via /IWXBE/CONFIG. For administration, testing as well as monitoring the transcation /IWXBE/EEE_SUPPORT is recommended., collecting all relevant transactions in the EEE context.
### Resources
#website[Enterprise Event Enablement | SAP Help Portal](https://help.sap.com/docs/SAP_S4HANA_ON-PREMISE/810dfd34f2cc4f39aa8d946b5204fd9c/c200f98fadb64ff1828ed5696c86fca2.html?locale=en-US)