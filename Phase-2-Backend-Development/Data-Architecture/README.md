# Phase 2: Backend Development & Configurations - Data Architecture

## Overview
This phase focuses on building the core backend setup for the Licensed Software Request catalog item. It establishes the Update Sets, catalog configuration, workflow design, and table data mapping required to automate the request and fulfillment lifecycle in ServiceNow[cite: 1].

---

## Key Configuration Steps

### 1. Update Set Setup
- Created a custom **Update Set** to track and capture all backend customizations, catalog configurations, and workflow definitions for easy deployment across environments[cite: 1].

### 2. Catalog Item & Variables Setup
- Configured the **Licensed Software Request** catalog item under the Service Catalog[cite: 1].
- Defined user variables (e.g., Software Application, Business Justification, Asset Tag) to capture request details[cite: 1].

### 3. Workflow & Automation Setup
- Built workflow execution logic using Flow Designer / Workflow Editor[cite: 1].
- Integrated automatic approval routing to the requestor's manager[cite: 1].
- Configured conditional task creation upon approval[cite: 1].

---

## Data Architecture & Table Mapping

The end-to-end data lifecycle is mapped across the primary ServiceNow request tables[cite: 1]:

| Table Label | System Name | Role in Architecture |
| :--- | :--- | :--- |
| **Request** | `sc_request` (REQ) | Top-level container generated upon order submission[cite: 1]. |
| **Requested Item** | `sc_req_item` (RITM) | Individual line item tracking request specifications and workflow execution[cite: 1]. |
| **Catalog Task** | `sc_task` (SCTASK) | Fulfillment task generated and assigned to the technical team for installation[cite: 1]. |
| **Approval** | `sysapproval_approver` | Holds manager approval state prior to task generation[cite: 1]. |

---

## Request Execution Flow

```text
User Request (Catalog Item) 
   └── sc_request (REQ)
         └── sc_req_item (RITM)
               ├── Manager Approval (sysapproval_approver)
               └── Fulfillment Task: sc_task (SCTASK)
