# ValcoMed
Hospital RBAC simulation with Vault, Falco, and containerized role isolation

## What this project does
ValcoMed orchestres a zero-trust, role-based access control system in a mock hospital setting. It simulates multiple user roles, each with diffrent containers, Vault policies, and Falco monitoring rules.

The system enforces
+ Least Privelage
+ Runtime threat detection - Falco
+ Reproducible infrastructure - Nix Flakes + Ansible + Tailscale
+ Observability - Prometheus + Grafana

## Overview

| Stack  | Role |
| ------------- | ------------- |
| Docker  | Separate containers for diffrent roles  |
| Hashicorp Vault  | Policies for role based access and rotating keys  |
| Falco  | Monitors runtime behavior, kills unauthorized privilege escalations   |
| Prometheus + Grafana  | Collects metrics and visualizes container health + Falco events  |
| Discord/Slack Webhook  | Real time alerts for container health + Falco kills  |
| Ansible  | Server Setup  |
| Nix Flake  | Reproducable, declarative system after inital ansible setup  |
| Tailscale  | Secure connection to server via ssh and closed firewall ports  |


# WORK IN PROGRESS !!
