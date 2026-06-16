# Azure Infrastructure Operations Blueprint

This repository shows a practical Azure infrastructure operations blueprint aligned with L2/L3 cloud support, hybrid infrastructure, security baseline, monitoring and operational readiness.

## Purpose

The goal is to demonstrate how I would structure a small production-style Azure environment with clear standards for:

- Resource groups and naming
- VNets, subnets, NSGs and route tables
- Azure Bastion for secure admin access
- Diagnostics and Log Analytics
- Azure Backup readiness
- Tagging and cost ownership
- Basic governance using Azure Policy concepts
- Operational handover documentation

## Architecture Overview

```text
Internet / Admin User
        |
        | Secure admin access
        v
Azure Bastion
        |
        v
Hub / Workload VNet
  |-- Management Subnet
  |-- Application Subnet
  |-- Data Subnet
  |-- Private Endpoint Subnet
        |
        v
Azure Monitor + Log Analytics + Backup Vault
```

## What this project demonstrates

- Azure infrastructure design thinking
- Network segmentation using subnet and NSG patterns
- Diagnostic settings and monitoring readiness
- Operational documentation suitable for handover to run teams
- Bicep/PowerShell-based repeatable deployment approach

## Repository Structure

```text
.
├── bicep/
│   ├── main.bicep
│   └── parameters.dev.json
├── scripts/
│   ├── deploy.ps1
│   └── validate-environment.ps1
├── runbooks/
│   ├── incident-triage.md
│   ├── change-implementation-checklist.md
│   └── operational-handover.md
└── docs/
    ├── naming-and-tagging-standard.md
    └── security-baseline.md
```

## Skills Highlighted

Azure VMs, VNets, NSGs, route tables, Azure Bastion, Azure Monitor, Log Analytics, Azure Backup, Azure Policy concepts, RBAC, PowerShell, Bicep, Git and ITSM-style documentation.

## Disclaimer

This is a portfolio/lab blueprint. It uses placeholders and does not contain any customer data, secrets or production identifiers.
