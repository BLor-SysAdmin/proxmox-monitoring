# Enterprise Infrastructure Telemetry & Observability Pipeline

## Homelab Network Topology
![Homelab Master Network Topology](https://raw.githubusercontent.com/BLor-SysAdmin/HTC-Network-Administration-Labs/main/homelab-topology-blueprint.png)

## Executive Architecture Overview
This production-grade monitoring pipeline establishes continuous infrastructure visibility and time-series resource tracking across a heterogeneous multi-OS network layout. Built leveraging a containerized microservices model, the stack isolates monitoring dependencies, prevents metric storage fragmentation, and provisions real-time metrics for capacity planning and proactive troubleshooting.

## System Topology Blueprint
*   **Hypervisor Layer:** Type-1 Proxmox VE Cluster Node
*   **Database Engine:** Prometheus (Time-Series Metrics Scraper Platform)
*   **Visualization Studio:** Grafana NOC Cockpit Analytics Dashboard
*   **Endpoint Agents:** Node Exporter (Linux Systems & FreeBSD/OPNsense Core)
*   **Storage Profiles:** Isolated Docker Managed Volumes (Data Persistence Baseline)

## Technical Features Implemented
1.  **Zero-Loss Data Persistence:** Configured dedicated, decoupled local volume blocks ensuring historical telemetry logs and custom dashboard templates survive routine container system updates, hard reboots, and crashes.
2.  **Isolated Virtual Network Sandboxing:** Bound application nodes to a distinct backend virtual network bridge (`monitoring`), isolating core telemetry collection vectors from unauthorized adjacent lab networks.
3.  **High-Density NOC Visualization:** Automated dashboard instrumentation (Grafana ID: 1860) capturing real-time CPU thread execution metrics, RAM exhaustion ceilings, disk I/O seek delay variations, and network transit loads on a continuous 15-second scrape loop interval.

## Deployment Instructions
To instantiate this observability pipeline across an internal Docker node environment, copy these repository manifests and run:
```bash
sudo docker compose up -d
```
