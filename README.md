# IoT – CoAP, MQTT & Energy Consumption Analysis

This repository, covering Wireshark packet sniffing for CoAP/MQTT and energy consumption estimation for IoT devices based on measured data.

## Project Overview
The project has two main parts:

1. **Packet Sniffing & Analysis (Wireshark)**
   - CoAP confirmable/non-confirmable GET and PUT requests
   - MQTT client connections, subscriptions, and Last Will messages
   - Topic filtering with/without wildcards
   - Retained MQTT publishes
   - 
2. **Energy Consumption Estimation**
   - Analysis of CSV power measurement files:
     - `transmission_power.csv`
     - `deep_sleep.csv`
     - `sensor_read.csv`
   - Computation of:
     - Cycle duration
     - Energy per cycle

## Features
- **Wireshark Filters** for isolating specific CoAP/MQTT traffic patterns.
- **Statistical results** for:
  - Failed confirmable PUT requests
  - Equal confirmable & non-confirmable GET counts
  - MQTT client ID extraction
  - Last Will topic analysis
  - Retained message count

## How to Use
1. **Packet Analysis**:
   - Open `.pcap` file in Wireshark.
   - Apply documented filters to reproduce results.

2. **Energy Analysis**:
   - Open CSV files and compute energy values using the provided formulas.
   - Compare results with the report for validation.

## Key Results
- **Packet Analysis**:
  - 22 failed confirmable PUT requests
  - 3 resources with equal confirmable & non-confirmable GET requests
  - 4 MQTT clients using multi-level wildcards
  - 1 MQTT client with a "university" Last Will topic
