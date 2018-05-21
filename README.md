# Overview
A serverless real-time end-2-end ML pipeline built entirely on Google Cloud Platform services - AppEngine, PubSub, Dataflow, BigQuery and Cloud ML

The architecute of datahem consists of loosely coupled parts to enable future replacements and extensions of parts.

datahem is licensed under [MIT](https://opensource.org/licenses/MIT)

# datahem ecosystem
* **[tracker](https://github.com/mhlabs/datahem.tracker):** Send data to datahem collector, currently supporting Google Analytics javascript tracker
* **[collector](https://github.com/mhlabs/datahem.collector):** Collect data sent from trackers and publish the data on pubsub, currently running on Google App Engine Standard (Java)
* **[processor](https://github.com/mhlabs/datahem.processor):** Process bounded and unbounded data and write to PubSub and BigQuery, currently using Google Dataflow (Apache Beam) and supports processing of Google Analytics hits and AWS Kinesis events
* **[serializer](https://github.com/mhlabs/datahem.serializer):** Serialize structured data in datahem, currently using protocol buffers
* **[infrastructor](https://github.com/mhlabs/datahem.infrastructor):** Infrastructure as code to easily setup API:s and services necessary for datahem, currently using Google Deployment Manager
* **predictor** (backlog) predictions made on streaming data
* **pseudonymizor** (backlog) pseudonymizing personal and/or sensitive data
* **ruler** (backlog) processing rules for personal data
* **activator** (backlog) serving predictions via REST/gRPC

# Setup
[Follow instructions in wiki how to set up the various parts in datahem](https://github.com/mhlabs/datahem/wiki/Setup)

# Background
datahem was started in June 2017 by [robertsahlin](https://github.com/robertsahlin) / [ML-engineer](https://github.com/ML-engineer). It was open sourced and officially brought under Mathem's mhlabs Github account and announced in May 2018.
