# Small Office Network Using Cisco Packet Tracer

## Project Overview

This project demonstrates the design and implementation of a small office network using Cisco Packet Tracer. The network consists of one router, two switches, and four PCs distributed across two different networks.

The objective is to configure IP addressing, default gateways, and router interfaces so that all devices can communicate successfully.

---

## Network Topology

Router
├── Switch 1
│   ├── PC0
│   └── PC1
│
└── Switch 2
├── PC2
└── PC3

---

## IP Addressing Scheme

| Device      | IP Address   | Subnet Mask   | Default Gateway |
| ----------- | ------------ | ------------- | --------------- |
| PC0         | 192.168.1.1 | 255.255.255.0 | 192.168.1.5     |
| PC1         | 192.168.1.2 | 255.255.255.0 | 192.168.1.5     |
| Router G0/0 | 192.168.1.5  | 255.255.255.0 | N/A             |
| PC2         | 192.168.2.1 | 255.255.255.0 | 192.168.2.5     |
| PC3         | 192.168.2.2 | 255.255.255.0 | 192.168.2.5     |
| Router G0/1 | 192.168.2.5  | 255.255.255.0 | N/A             |

---

## Router Configuration

### Configure Interface G0/0

enable

configure terminal

interface g0/0

ip address 192.168.1.5 255.255.255.0

no shutdown

exit

### Configure Interface G0/1

interface g0/1

ip address 192.168.2.5 255.255.255.0

no shutdown

end

---

## Verification

The following tests were performed:

* PC0 successfully pinged PC2
* PC1 successfully pinged PC3
* PC3 successfully pinged PC0
* PC2 successfully pinged PC1
* Router interfaces were verified using:

  * show ip interface brief

All devices were able to communicate successfully through the router.

---

## Skills Demonstrated

* Basic Network Design
* IPv4 Addressing
* Router Configuration
* Switch Connectivity
* Default Gateway Configuration
* Network Verification and Troubleshooting

---

## Files Included

* SmallOfficeNetwork.pkt
* topology2.png
* ping-test.png
* README.md
* modes.png
* access verification.png

---

## Author

Created as part of my CCNA and Networking learning journey using Cisco Packet Tracer.
