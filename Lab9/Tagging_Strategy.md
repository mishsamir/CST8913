# Azure Resource Tagging Strategy

## Purpose
This document outlines our tagging strategy for Azure resources to enable better cost tracking, resource management, and organizational alignment.

### Here is the sample diagram for a resource tagging strategy
<img width="798" alt="Screenshot 2025-03-15 at 1 13 18 PM" src="https://github.com/user-attachments/assets/06daa8da-2fae-445a-8faa-e832594e9fc5" />


## Tags

### Environment Tag
- **Name:** Environment
- **Value:** Test
- **Purpose:** Identifies the environment where the resource is deployed
- **Resources Applied To:** All resources (VMs, Storage, SQL Databases, etc.)

### Department Tag
- **Name:** Department
- **Value:** IT
- **Purpose:** Identifies the department responsible for the resource
- **Resources Applied To:** All resources (VMs, Storage, SQL Databases, etc.)

## Benefits of Tagging
1. **Cost Allocation:** Enables accurate attribution of costs to departments
2. **Resource Organization:** Simplifies resource management and filtering
3. **Automation:** Facilitates automated processes based on tags
4. **Governance:** Supports compliance with organizational policies

## Implementation Process
1. Apply tags during resource creation
2. Enforce tagging policy through Azure Policy
3. Review and update tags quarterly

## Reporting
Tags can be leveraged in Cost Analysis reports to filter and group resources by environment and department.
