# Monitoring with Prometheus and Grafana

This repository provides a quick start to set up a Prometheus stack containing Prometheus, Grafana, and other related services for monitoring website uptime. Follow the steps below to get started:

## Pre-requisites

- This tutorial assumes you are running on a Raspberry Pi. You can use your own service provider, but I recommend using Portainer.
- Install and configure Prometheus and Grafana using the instructions below.

## Installation & Configuration

1. Run the following command for a one-click install experience in Portainer:

''bash
Dashboard -> Stacks > Add Stack -> docker-compose.yaml contents

2. Add the prometheus.yaml file to the Raspberry Pi (host) for Prometheus

''bash
Login to your Raspberry Pi -> cd /data/compose/2/config/ & copy prometheus.yaml 

3. Restart Prometheus Container in Portainer

''bash
Dashboard -> Stacks > Container > Restart

4. Login to Grafana and configure Prometheus as data source 

Services Created
Prometheus: Data Aggregator (Port: 9090)
Alert Manager: Adds Alerting for Prometheus Checks (Port: 9093)
Grafana: UI to Show Prometheus Data (Port: 3000, Username: admin, Password: 9uT46ZKE)
Node Exporter: Data Collector for Computer Stats (Port: 9100)
CA Advisor: Collects resource usage of Docker containers (Port: 8080)
