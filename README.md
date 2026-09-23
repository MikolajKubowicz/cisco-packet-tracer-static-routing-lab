Cisco Packet Tracer – Static Routing & Network Security Lab

This project is a Cisco Packet Tracer lab completed for NET 377. It demonstrates basic router configuration, IPv4 addressing, static routing, HTTP connectivity, SSH remote access, and an extended access control list (ACL).

Project Overview

The lab builds a small network with:

GZ-Client

GZ-Server

GZ-CE router

Internet router

Pub-Router

Cisco switch

The goal was to configure the devices so that all required networks could communicate, verify connectivity, enable network services, and then apply an ACL that blocks inbound HTTP traffic while allowing other IP traffic.

Network Addressing

Device

Interface

IPv4 Address

Prefix

GZ-Client

Fa0

33.1.1.99

/24

GZ-Server

Fa0

33.1.1.19

/24

GZ-CE

Gi0/0/1

33.1.1.254

/24

GZ-CE

Gi0/0/0

82.16.5.29

/30

Internet

Gi0/0/0

82.16.5.30

/30

Internet

Gi0/0/1

102.19.0.1

/30

Pub-Router

Gi0/0/0

102.19.0.2

/30

Pub-Router

Loopback0

2.2.2.2

/32

What I Configured

Router Setup

Configured router hostnames

Assigned IPv4 addresses and subnet masks

Enabled router interfaces

Verified interfaces with show ip interface brief

Static Routing

Configured default routes on GZ-CE and Pub-Router

Configured specific static routes on the Internet router

Verified end-to-end connectivity with ping

Verified routing paths with traceroute / tracert

HTTP Service

Enabled HTTP on GZ-Server

Tested TCP port 80 connectivity with Telnet

SSH

Configured a local SSH user on Pub-Router

Configured a domain name

Generated a 1024-bit RSA key

Enabled SSH on VTY lines

Successfully connected remotely to Pub-Router using SSH

Access Control List

Created an extended ACL named INCOMING-ACL that:

Denies inbound TCP traffic with destination port 80

Permits all other IP traffic

Is applied inbound on GZ-CE interface Gi0/0/0

The ACL was verified by confirming that traceroute still succeeded while Telnet to port 80 was blocked.

Skills Demonstrated

Cisco IOS CLI

IPv4 addressing

Subnet masks

Static routing

Default routes

Connectivity troubleshooting

Ping and traceroute

HTTP/TCP testing

SSH configuration

RSA key generation

Extended ACLs

Packet filtering

Cisco Packet Tracer

Repository Files

.
├── README.md
├── packet-tracer/
│   └── Lab1-Mikolaj-Kubowicz-v1.pkt
└── report/
    └── Lab1-PT-Answers.pdf

Opening the Packet Tracer File

The .pkt file requires Cisco Packet Tracer 8.2.2 or later. GitHub does not render Packet Tracer files directly in the browser, so download the file and open it locally in Cisco Packet Tracer.

Notes

This repository is intended to document my hands-on networking and cybersecurity work. Credentials used during the original classroom exercise are intentionally not documented here.

Author

Mikolaj Kubowicz
Computer Science & Cybersecurity
