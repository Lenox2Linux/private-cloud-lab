# Architecture

## High-Level Design
This private cloud lab uses Tailscale as the secure remote access layer and Nextcloud as the main self-hosted cloud platform.

## Basic Flow
Client Device -> Tailscale Network -> Lab Host -> Nextcloud

## Main Components
- Client device used to access the lab remotely
- Tailscale secure private network connection
- Linux-based host running the services
- Nextcloud application providing private cloud functionality

## Purpose of the Design
The design allows private access to a self-hosted cloud service without relying on broad public exposure. It also provides a practical way to learn service deployment, remote access, and administrative documentation.

## Design Value
This setup demonstrates a small but realistic private cloud implementation with security-conscious access control and organized documentation.
