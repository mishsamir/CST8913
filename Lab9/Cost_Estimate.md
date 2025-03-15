# Azure Cost Estimation

## Overview
This document provides a cost estimate for deploying a simple 2-tier application in Azure.

## Configuration Details

### Frontend
- **Resource Type:** Virtual Machine
- **Size:** Standard B2s (2 vCPUs, 4 GB RAM)
- **Storage:** 64 GB Standard SSD
- **Estimated Monthly Cost:** $81.03

### Backend
- **Resource Type:** Virtual Machine
- **Size:** Standard D2s_v3 (2 vCPUs, 8 GB RAM)
- **Storage:** 128 GB Standard SSD
- **Estimated Monthly Cost:** $81.03

### Database
- **Resource Type:** SQL Database
- **Configuration:**
  - Region: Canada Central
  - Type: Single Database
  - Purchase Model: vCore
  - Service Tier: General Purpose
  - Compute Tier: Provisioned
  - Generation: Gen5
  - vCores: 2
  - Data Storage: 50 GB
- **Estimated Monthly Cost:** $417.90

### Networking
- **Outbound Data Transfer:** 200 GB
- **Estimated Monthly Cost:** $9.75

## Total Estimated Monthly Cost: $589.71
