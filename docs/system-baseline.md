# System & Network Baseline

## System

- Platform: Android / Termux
- Android: 11
- Linux Kernel: 4.19.127
- Architecture: ARMv7 (32-bit)
- User: u0_a203

## Network

- Interface: wlan0
- Status: UP
- IPv4: 192.168.1.243/24
- Gateway: 192.168.1.1
- Network: 192.168.1.0/24
- MTU: 1500

## Connectivity Tests

### Gateway

Command:

`ping -c 4 192.168.1.1`

Result:

- 4/4 packets received
- 0% packet loss
- Average latency: 5.723 ms

### Internet

Command:

`ping -c 4 1.1.1.1`

Result:

- 4/4 packets received
- 0% packet loss
- Average latency: 29.375 ms

### DNS

Command:

`nslookup google.com`

Result:

- DNS Server: 8.8.8.8
- Domain resolution successful

### HTTPS

Command:

`curl -I https://google.com`

Result:

- HTTP/2 301
- Redirect to `https://www.google.com/`

## Summary

The network baseline successfully verified the interface, IP configuration, routing, gateway connectivity, internet connectivity, DNS resolution, and HTTPS connectivity.	
