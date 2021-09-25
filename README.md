# logstash

This Logstash Configs are for custom Finacle Core Banking and Ebanking Logfiles. These include Finacle Web Access Logs, cbclogs, cdcilogs, uniserevtlogs, febalog, hiflog, msglog,fatlog,errlog etc. I also have brokendown/parsed the different finacle scripts pmtadd, executefinaclescript, getcorpretailindicator, custinq, retcustinq etc.

#Architecture

Filebeats are installed on the Finacle WebServers, AppServers and CoreServers. Logs are then shipped into different Kafka Topics. Logstash then uses the Kafka input plugin to subscribe to the different topics created for the logs and goes on to process/parse the logs and index into elasticsearch/opensearch.
