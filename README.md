# Private Self-Hosted Cloud with Nextcloud AIO and Tailscale

## Project Overview

This project documents the build of a private self-hosted cloud environment in a home lab using **Nextcloud AIO**, **Docker**, and **Tailscale** on an Ubuntu Server running on a Mac mini.

The goal was to create a secure personal cloud that could be accessed remotely **without exposing the home network to the public internet through port forwarding**.

During the build, the original design involved public access through a domain and router forwarding. However, after identifying the added complexity and risk of a double-router environment, the design was changed to use **Tailscale** for private encrypted remote access.

This project became more than just an application install. It became a practical exercise in:

- self-hosting
- Docker deployment
- network troubleshooting
- secure remote access design
- service recovery
- architecture decision-making
- documenting technical work clearly

---

## Objective

Build a private cloud service in a lab environment that allows secure remote access to files and services without unnecessary public exposure.

---

## Key Technologies Used

- **Nextcloud AIO**
- **Docker**
- **Ubuntu Server**
- **Tailscale**
- **Mac mini**
- **Home lab networking**
- **Private remote access**
- **HTTPS reverse proxy through Tailscale Serve**

---

## Lab Environment

### Main Devices

- **Mac mini**
  - Role: application/service host
  - OS: Ubuntu Server
  - Hosted services: Nextcloud AIO and related containers

- **Lenovo ThinkPad T14**
  - Role: management workstation
  - Used to remotely access and manage the Mac mini

- **Lenovo M920**
  - Role: main infrastructure server / Proxmox hypervisor
  - Planned for future infrastructure services such as Pi-hole and additional VMs

### Network Path


ISP → AX3200 home router → AX50 lab router → GS308E managed switch → Mac mini
