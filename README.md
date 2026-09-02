# MEC Defense: Securing Smart Stadium Critical Infrastructure

## Overview
This repository contains the project report and architectural documentation for a network security framework designed for high-density environments, such as smart stadiums. 
My main contribution to this project was the implementation of robust network isolation, traffic segmentation, and automated firewall enforcement to prevent lateral movement attacks and ensure high-performance data flow.


## Key Network Engineering Features

*   **VXLAN-Based Segmentation:** Implements VXLAN encapsulation (Layer 2 MAC frames within Layer 3 UDP packets) to achieve deep network isolation, bypassing the physical limitations of standard 802.1Q VLANs in the virtualized environment.
*   **Stateful Boundary Control:** Utilizes UFW (Uncomplicated Firewall) and the underlying Linux Netfilter framework to enforce strict ingress and egress filtering between network segments.
*   **Anti-Spoofing (BCP 38):** Integrates strict Interface Binding with the Linux kernel's Unicast Reverse Path Forwarding (uRPF) to silently drop packets with spoofed internal IPs arriving on incorrect physical interfaces.
*   **Automated Threat Mitigation:** Features a Python-based webhook service that dynamically updates UFW rules to block unauthorized IP addresses in real-time, coupled with a strict whitelist to ensure critical machine availability.

## Technologies & Protocols Used
*   **Networking:** VXLAN, UDP, TCP/IP
*   **Security:** UFW, iptables, uRPF (BCP 38 Anti-spoofing)
*   **Automation:** Python (Webhook-based rule management)



## Authors and Acknowledgements
This project was developed at the **Universidade de Aveiro / Instituto de Telecomunicações**.
*   **Project Team:** José Fernandes, Diogo Ferreira, Rúben Franco, Diogo Carvalho, Gonçalo Martins, Tiago Rocha.
*   **Supervisors:** Professor Daniel Corujo, Professor Vitor Cunha.
