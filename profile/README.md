# WeeWX-MQTT

This organization is for a collection of repositories that bring MQTT functionality to WeeWX.

## [Subscribing](https://github.com/bellrichm/WeeWX-MQTTSubscribe)

This repository provides WeeWX with the ability to subscribe to MQTT topics and the data to the WeeWX processing pipeline. It can be run as either a WeeWX driver or a WeeWX service.
MQTT messages with json, keyword/values, or individual values can be processed.

When running as a driver, WeeWX loop packets are created passed to WeeWX.
WeeWX processing then takes these, creates archive records, runs other services, and generates reports.

When running as a service, either loop packets or archive records can be augmented with the data from MQTT.

Note: This repository is not currently a part of this organization. It can be found [at this repository](https://github.com/bellrichm/WeeWX-MQTTSubscribe). The goal is to have it moved in 2026.

## [Publishing](https://github.com/weewx-mqtt/publish)

This repository provides WeeWX with the ability to publish WeeWX data to MQTT.
MQTT messages content can be either json, keyword/values, or individual values.
Data can be published to multiple topics, each with its own format.
Each topic can be configured to publish on a new loop packet, new archive record, or both.

## [Replicating](https://github.com/weewx-mqtt/replicate)

This repository provides a "lightweight" database replication using MQTT V5 request/response capability.

This is very much experimental, and I am not sure there is such a thing as "lightweight replication".
