# SOC-LAB2026

## Decription
This project focuses on creating a cloud-native honeypot in Microsoft Azure with the goal of logging and analyzing traffic from potential attackers. 
The honeypot is created using a virtual machine that is intentionally left open to the public internet to attact malicious activity. All incoming traffic and attack attempts are logged through a configured log forwarding system and the data stored in a centralized repository.
The repository is connected to a Security Information and Event Management (SIEM) system for monitoring and hreat analysis. 
Finally, the project includes development of an attack visualization map that provides a geographic representation of the attacks.

## Objectives
Deploy a cloud-based honeypot in Azure
Capture real-world attacks
CEntralize and monitor logs in a SIEM platform (Sentinel)
Analyze attack data using KQL queries
Use an attack map to visualize attacks

## Cloud Architecture
                    Public Internet (Threat Actors)
                              │
                              ▼
        ┌────────────────────────────────────┐
        │ Azure VM (Honeypot / Attack Surface)│
        │ - Virtual machine with all inbound traffic allowed      |         
        └────────────────────────────────────┘
                              │
                              ▼
        ┌────────────────────────────────────┐
        │            Log Analytics           │
        │ - Log analytics workspace          │
        └────────────────────────────────────┘
                              │
                              ▼
        ┌────────────────────────────────────┐
        │            SIEM:                   │
        │ - Microsoft Sentinel               │
        └────────────────────────────────────┘
                              │
                              ▼
        ┌────────────────────────────────────┐
        │ Threat Intelligence Visualization  │
        │ - KQL Queries                     |  
        │ - Attack map Dashboard           │
        └────────────────────────────────────┘

## Technologies Used
Microsoft Azure.

MIcrosoft Sentinel.

Log Analytics Workspace.

Windows.

Kusto Query Language.

GeoIP data enrichment.

## Deployment Steps
  ## Azure Setup
Create Resource Group.

Deploy Virtual Network.

Create virtual machine.

Assign Public IP address (leave as default).

## Honeypot Configuration
Open all inbound NSG rules.

Enable remote access exposure.

## Log Validation
Confirm failed login attempts.
## Sentinel Setup
CreateLog Analytics Workspace.

Enable Microsoft Sentinel.

Connect virtual machine.

## Data analysis
Use KQL to analyze data.
## Attcak map visualization
Import geoip database.

Map attacker IP addresses to locations.

Visualize attack distributions.
