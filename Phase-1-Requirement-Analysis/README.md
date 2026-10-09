# Phase 1: Requirement Analysis & Planning

## Overview
This folder contains the planning and foundational architecture for automating software installation requests in ServiceNow. 

---

## Key Modules & Breakdown

### 1. Business Objectives
- Streamline employee software licensing requests through a self-service portal.
- Reduce manual administrative overhead by automating approval workflows and provisioning tasks.
- Maintain compliance and tracking for licensed software assets across the organization.

### 2. Functional Scope
- **Service Catalog Item:** Create a dedicated "Licensed Software Request" item.
- **Form Variables:** Capture key user details (Application Name, Business Justification, Asset Tag/Device ID).
- **Workflow & Approval:** Route requests dynamically to the Requestor's Manager for approval prior to fulfillment task creation.
- **Data Architecture:** Mapped across `sc_request`, `sc_req_item` (RITM), and `sc_task` tables.

### 3. Stakeholder Mapping
- **End Users / Employees:** Submit requests and track status via the Service Catalog.
- **Line Managers:** Review and approve/reject software requests.
- **IT / License Fulfillment Team:** Process approved software installation tasks.
- **System Administrator:** Configure catalog forms, flow execution logic, and update set deployments.

### 4. Execution Roadmap
1. Complete requirement gather and table schema mapping.
2. Build catalog item variables and layout.
3. Configure Flow Designer trigger and manager approval routing.
4. Export and validate baseline configuration via Update Set.



