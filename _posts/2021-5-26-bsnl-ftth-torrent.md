---
layout: default
title: BSNL FTTH setup for Torrent seeding
---
## BSNL ONT setup
Model: Alphion AONT-100C rev 1.0
IP: 192.168.1.251
username: root
pwd: google chromium

## Wifi router settings
Model: Xiaomi Mi 3C
IP: 192.168.31.1
pwd: same as wifi pwd

## LAN IP vs WAN IP
LAN IP is your internal (local) IP address that's just for your home devices in your local network. 
The LAN IP won't work outside of the local network.
Ex: 192.168.1.5

WAN IP is your unique address for the web that your ISP gives you (gives your router and you).
You will be uniquely identified by this IP, by the servers in the internet all over the world.
Ex: 117.100.51.10

## Disable DHCP and set static IP - Wifi router 
- Login to Wifi rouer IP
- `Settings -> LAN settings -> disable 'DHCP Server'`
- `Settings -> Network settings -> Network settings`. set static IP similar to following:
  - 192.168.1.X(23) - static IP
  - 255.255.255.0   - subnet
  - 192.168.1.251   - gateway
  - 192.168.1.251   - DNS1

## Port forwarding - ONT router
- Login to ONT router IP
- `Advanced -> port forwarding`
  - Torrent             - Application name
  - Y-Y (25000-25000)   - start-end port
  - TCP/UDP (both)      - protocol
  - 192.168.1.X(23)     - To IP address
  - 8080-8080           - start-end port
  - check the `Enable` box and click Apply
### If the above port forwarding doesnot start the torrent seeding
- `Advance -> Firewall`
- Enable `Dmz` and click Apply


