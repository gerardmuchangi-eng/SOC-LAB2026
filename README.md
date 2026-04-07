# SOC-LAB2026

## Description
This project focuses on creating a cloud-native honeypot in Microsoft Azure with the goal of logging and analyzing traffic from potential attackers. 
The honeypot is created using a virtual machine that is intentionally left open to the public internet to attract malicious activity. All incoming traffic and attack attempts are logged through a configured log forwarding system and the data stored in a centralized repository.
The repository is connected to a Security Information and Event Management (SIEM) system for monitoring and threat analysis. 
Finally, the project includes development of an attack visualization map that provides a geographic representation of the attacks.

## Objectives
Deploy a cloud-based honeypot in Azure
Capture real-world attacks
Centralize and monitor logs in a SIEM platform (Sentinel)
Analyze attack data using KQL queries
Use an attack map to visualize attacks

## Cloud Architecture
                    Public Internet (Threat Actors)
                              │
                              ▼
        ┌────────────────────────────────────┐
        │ Azure VM (Honeypot / Attack Surface)│
        │ - Virtual machine with all inbound 
           traffic allowed                   |         
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
        │ - KQL Queries                      |  
        │ - Attack map Dashboard             │
        └────────────────────────────────────┘

## Technologies Used
Microsoft Azure.

Microsoft Sentinel.

Log Analytics Workspace.

Windows 2025 server data center.

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
Create Log Analytics Workspace.

Enable Microsoft Sentinel.

Connect virtual machine.

## Data analysis
Use KQL to analyze data.

## Attack map visualization
Import geoip database.

Map attacker IP addresses to locations.

Visualize attack distributions.

## Screenshots

## Vnet
<img width="1920" height="1080" alt="Screenshot (18)" src="https://github.com/user-attachments/assets/6434b557-155a-483d-8895-c3170ba09598" />

## Virtual Machine
<img width="1920" height="1080" alt="Virtual Machine" src="https://github.com/user-attachments/assets/c729efea-3242-42bd-9dc9-046f69c0b7e3" />

  ## Resource Group
<img width="1920" height="1080" alt="Resource Group" src="https://github.com/user-attachments/assets/408fdc8c-6bdc-4623-91dd-e51e6c70c8fb" />

## WAtchlist
<img width="1920" height="1080" alt="Watchlist" src="https://github.com/user-attachments/assets/111217cf-6dec-4a92-a8a7-2b7eaa00906c" />

## Watchlist embedded in Log analytics
<img width="1920" height="1080" alt="Watchlist embedded in log analytics" src="https://github.com/user-attachments/assets/8228e804-8fe1-4310-82bf-e17c82211a1c" />

## KQL to return failed log on logs
<img width="1920" height="1080" alt="KQL to return failed logon logs" src="https://github.com/user-attachments/assets/8c8d5f53-11ac-42d6-84b6-53c4b9da6ec5" />

## KQL to return failed logon logs with location included
<img width="1920" height="1080" alt="KQL to return Failed logon logs with location included" src="https://github.com/user-attachments/assets/67f0d1aa-3eb7-44fc-9f69-99154f571830" />

## Attack Map
<img width="1920" height="1080" alt="Attack Map" src="https://github.com/user-attachments/assets/a6305dbc-3eb4-4207-be38-4b69ab193455" />

## Key Features
Real-time attack monitoring.

Cloud-native SIEM.

Hands-on SOC workflow simulation.

Global threat visualization.

## Security Warning!!
This environment is intentionally insecure and should not be used in real-life production systems. It is strictly for educational purposes.

## Acknowledgements
Inspired by Azure SOC lab cybersecurity training environments and Microsoft Sentinel hands-on labs.

