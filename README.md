# 🌐 Networking Project: Securing and Segmenting Enterprise Infrastructure

Welcome to my Networking Project repository. 

This project details the end-to-end implementation of a segmented, secure internal network for NetCore Systems Ltd. using Cisco Packet Tracer. The solution emphasizes operational assurance, policy-based controls, and scalable design—reflecting my approach to efficient, risk-aware IT infrastructure.

# 🔎 Project Summary: 

For modern organizations, robust network segmentation and access controls are foundational to both security and operational integrity. In this project, I architected and configured a departmental network leveraging VLANs, DHCP, ACLs, and centralized services to meet real-world business and compliance requirements.

# 🛠️ Key Technical Highlights

## Segmented Network Design:
Architected three isolated subnets (IT, Sales, HR), each with distinct address spaces, centralized gateway, and switch infrastructure.


## Centralized DHCP & Service Deployment:
Deployed a central IT server providing DHCP for all segments, plus HTTP and FTP services for secure file and web access.


## Access Control & Security:
Applied an extended Access Control List (ACL) to enforce business policy: Sales cannot ping the IT segment but can access required services.


## Stepwise Validation:
Systematic functional and security testing confirmed all PCs received correct addresses, all legitimate services remained reachable, and inter-department policies were enforced with zero over-blocking.

# 🚀 Implementation Walkthrough 

## Network Topology
Cisco 2911 router, three 2960 switches, six workstations, and central IT server

Each department mapped to its own /24, with the router as primary gateway


*completed topology with interface labels shown*
<img width="1166" height="627" alt="image" src="https://github.com/user-attachments/assets/29af046e-eb26-44a6-a753-89bd4f49cfea" />

*completed topology with device names shown*
<img width="1166" height="626" alt="image" src="https://github.com/user-attachments/assets/67fe6d97-ea95-4b94-8629-1308449a44a8" />






## Configuration & Verification

### Static Address for Server

IT server at 192.168.10.2, ensuring consistent service discovery


### Router Subnet Interfaces

#Configured for each department:
  interface gigabitEthernet 0/0  
    ip address 192.168.10.1 255.255.255.0  
    no shutdown# 
  
#...repeated for Sales (G0/1) and HR (G0/2)

Verified all interfaces were up

<img width="622" height="442" alt="image" src="https://github.com/user-attachments/assets/5092260d-88f9-4cc1-b815-1d33a77d2dac" />



### Centralized DHCP with Relay (Helper Address)

Separate DHCP pools for each department

Helper addresses configured so non-IT segments relay requests to the server

Each PC received correct departmental address

<img width="650" height="295" alt="image" src="https://github.com/user-attachments/assets/03d69c88-9bc9-4faa-bf23-006a761822fa" />



### HTTP and FTP Service Enablement

Internal website live at http://192.168.10.2

<img width="1502" height="537" alt="image" src="https://github.com/user-attachments/assets/52ac6c71-3b78-4a59-8930-e751584d4f9b" />

FTP user technova for file operations

<img width="1477" height="330" alt="image" src="https://github.com/user-attachments/assets/d3a112a2-f1a3-4f76-a65b-3819936abb83" />



## 🧪 Testing and Controls

### Base Connectivity:
Confirmed all departments could communicate and access core services before policy enforcement.


### Browser & FTP Verification: 
Validated HTTP and FTP services across all segments.


### ACL Enforcement:

Blocked Sales-to-IT pings using a precise ACL.

Verified that legitimate business services (HTTP/FTP) remained reachable from Sales.

Ensured HR retained full inter-segment access as per requirements.

All results supported by direct command output and status screenshots.

<img width="1477" height="357" alt="image" src="https://github.com/user-attachments/assets/3681b8c1-10cc-4f11-98d0-f59262415bc3" />

<img width="1475" height="362" alt="image" src="https://github.com/user-attachments/assets/599b1bae-d06b-41d5-b158-1c6e3b823a58" />

<img width="1476" height="357" alt="image" src="https://github.com/user-attachments/assets/7c97799c-ee55-45d4-9ec0-7dd97e07a8b3" />

<img width="1491" height="392" alt="image" src="https://github.com/user-attachments/assets/242f10d9-d5b9-4361-9e6c-d561af26a35e" />

<img width="1466" height="217" alt="image" src="https://github.com/user-attachments/assets/4375e972-6aff-4f25-bf42-0f5d4a22b1df" />


# 🎯 Value Delivered
## Policy-Driven Security: 
Demonstrated granular enforcement of business policy via technical controls, without compromising legitimate workflows.
## Audit-Ready Documentation: 
Produced transparent, step-by-step evidence supporting infrastructure decisions and compliance assertions.
## Scalability: 
Designed an architecture that supports future departmental growth with minimal changes.

## 🤝 Collaboration
Developed in partnership with **10Alytics,** reinforcing a culture of practical, professionally aligned learning and infrastructure excellence.

## 📬 Connect

David Frempong

**LinkedIn:** [linkedin.com/in/david-frempong-48ab53337/](https://linkedin.com/in/david-frempong-48ab53337/) 




*Open to collaborations in network security, infrastructure governance, and operational risk management.*
