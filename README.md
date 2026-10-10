# ServiceNow Licensed Software Request Implementation

## Project Overview
End-to-end automated software request system built in ServiceNow using Service Catalog, Flow Designer, and dynamic manager approval routing.

---

## Phases Overview

### Phase 1: Requirement Analysis & Planning
- **Update Set XML:** [Download Phase 1 Update Set XML](./Phase-1-Requirement-Analysis/Download%20Phase%201%20Update%20Set%20XML.xml)
- **Phase Details:** [View Phase 1 Folder](./Phase-1-Requirement-Analysis/)
  
### Phase 2: Backend Development & Configurations Data Architecture

- **Data Architecture:** (A Data-Driven Workflow Approach)
- **Business Rules Configuration:**
  ![Business Rules Configuration](./Phase2/business_rule_config.png)
- **Automation Logic:**
  ![Automation Logic](./Phase2/automation_flow_design.png)

### Phase 3: Workflow & Flow Designer Setup
- Built flow triggering on `sc_req_item` submission.
- Added **Ask For Approval** action routing dynamically to the Requestor's Manager.

### Phase 4: Testing & Deployment
- Validated lifecycle across `sc_request`, `sc_req_item`, and `sc_task`.
- Exported configurations via Update Set (`.xml`).

---

## File Structure
- `/Update-Sets/`: Exported `.xml` file containing all configurations.
- `/Phase-1-Requirement-Analysis/`: Workflow & requirement planning docs.
- `/Phase-2-Service-Catalog/`: Catalog item setup screenshots.
- `/Phase-3-Workflow-Design/`: Flow Designer execution context screenshots.
