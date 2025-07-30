# 📘 ECO Technical Document — Standard Template

> Standardized technical record for tracking and implementing industrial changes on SKD/CKD models.

---

## 1. 📦 Applied Models  
[Insert full list with naming variations, SKD/CKD, regional codes]

## 2. 📅 Implementation Date  
Example: Immediate / After approval / PA or PV Event / Specific date

## 3. 🔄 Type of Change  
- Coupled Change: `Yes` / `No`  
- Rework Required: `Yes` / `No`

## 4. 🎯 Reason for Change  
Objective and technical description — e.g., BOM adjustment, software update, process correction, etc.

## 5. 🧠 Technical Details  
**5.1 Affected Components**  
Example: SAA30114913 → SAA30114915  

**5.2 Software Versions / QPA / Consumption Info**  
App History: 1073  
Checksum: 0552A796  

**5.3 ECO HQ / Reference Codes**  
EKMP700810, DKLP300437, EKLO200699, etc.

## 6. 🏭 Application Location  
Specific area where the change will be implemented: PCB Main, LCM, SMT, Pulp Pack, etc.

## 7. 📝 Comments & Notes  
- Differences from previous versions  
- Model status (EOL, no production plan)  
- Expected impacts on production and testing

## 8. 🧩 Actions by Department  
- RnD: Conduct validations / Update work instructions  
- PE/MFG: Adjust process / Apply new method or version / Activate instrumentation  
- IQC/OQC/DQA/SQA: Perform inspections / PMP testing / Homologation  
- PCM/SMT: Manage inventory / Work order maintenance / Apply submaterials as per ECO  
- Instrumentation / Monitoring / ST/LB: Provide technical support / Option checking / Time planning  
- Materials: For awareness / consumption control

## 9. 📎 Attachments  
- Work instructions  
- BOM comparison (As-Is vs To-Be)  
- Test reports / ECO HQ documentation  
- Fumisso / Validation documents

---

# 🗃️ ECO Technical — Database & Markdown Structure

> This document outlines how standardized ECO model data can be represented using Markdown tables and structured in a relational database.

---

## 1. 📦 Table: eco_documents

| Field                | Type      | Description                                         |
|----------------------|-----------|-----------------------------------------------------|
| id                   | INT (PK)  | Unique identifier for the ECO                      |
| document_title       | VARCHAR   | Title of the technical document                    |
| applied_models       | TEXT      | List of impacted SKD/CKD models                    |
| implementation_date  | DATE      | Date the change will be applied                    |
| is_coupled_change    | BOOLEAN   | Coupled change (`true` = yes / `false` = no)       |
| requires_rework      | BOOLEAN   | Rework needed (`true` / `false`)                   |
| change_reason        | TEXT      | Technical description of the change                |
| application_area     | VARCHAR   | Location of implementation (PCB, LCM, etc.)        |
| comments             | TEXT      | General notes and observations                     |

---

## 2. 🔧 Table: technical_details

| Field             | Type      | Description                                        |
|-------------------|-----------|----------------------------------------------------|
| id                | INT (PK)  | Technical detail identifier                        |
| eco_id            | INT (FK)  | Reference to the main ECO document                 |
| component_from    | VARCHAR   | Previous component code                            |
| component_to      | VARCHAR   | New component code                                 |
| app_history       | VARCHAR   | Version history                                    |
| checksum          | VARCHAR   | Validation checksum code                           |
| reference_codes   | TEXT      | ECO HQ or related tracking codes                   |

---

## 3. 🧩 Table: department_actions

| Field             | Type      | Description                                        |
|-------------------|-----------|----------------------------------------------------|
| id                | INT (PK)  | Identifier                                         |
| eco_id            | INT (FK)  | Reference to the ECO document                      |
| department_name   | VARCHAR   | Department name (RnD, MFG, IQC, etc.)              |
| action_detail     | TEXT      | Description of planned or completed actions        |

---

## 4. 📎 Table: attachments

| Field             | Type      | Description                                        |
|-------------------|-----------|----------------------------------------------------|
| id                | INT (PK)  | Identifier                                         |
| eco_id            | INT (FK)  | Reference to the ECO document                      |
| attachment_type   | VARCHAR   | Type of file (BOM, report, instruction, etc.)      |
| file_path         | VARCHAR   | File path or URL to the attached asset             |

---

# 🗃️ ECO Technical — Database & Structure in Markdown

This document describes how standardized ECO model data can be represented in Markdown tables and later structured into a relational database.

---

## 1. 📦 Table: `eco_documents`

| Field               | Type        | Description                                       |
|--------------------|-------------|---------------------------------------------------|
| id                 | INT (PK)    | Unique identifier of the ECO                     |
| document_title     | VARCHAR     | Title of the technical document                  |
| applied_models     | TEXT        | List of applicable SKD/CKD models                |
| implementation_date| DATE        | Date of change implementation                    |
| is_coupled_change  | BOOLEAN     | Coupled change (true = yes / false = no)         |
| requires_rework    | BOOLEAN     | Rework required (true / false)                   |
| change_reason      | TEXT        | Technical description of the reason for change   |
| application_area   | VARCHAR     | Area of application (PCB, LCM, etc.)             |
| comments           | TEXT        | General remarks about the ECO                    |

---

## 2. 🔧 Table: `technical_details`

| Field            | Type      | Description                                      |
|------------------|-----------|--------------------------------------------------|
| id              | INT (PK)  | Technical identifier                             |
| eco_id          | INT (FK)  | Reference to the main ECO                       |
| component_from  | VARCHAR   | Old component code                               |
| component_to    | VARCHAR   | New component code                               |
| app_history     | VARCHAR   | Version history                                  |
| checksum        | VARCHAR   | Checksum code for validation                     |
| reference_codes | TEXT      | HQ ECO codes or related references               |

---

## 3. 🧩 Table: `department_actions`

| Field            | Type      | Description                                      |
|------------------|-----------|--------------------------------------------------|
| id              | INT (PK)  | Identifier                                       |
| eco_id          | INT (FK)  | Reference to the ECO document                    |
| department_name | VARCHAR   | Department name (RnD, MFG, IQC...)               |
| action_detail   | TEXT      | Description of planned/executed actions          |

---

## 4. 📎 Table: `attachments`

| Field            | Type      | Description                                      |
|------------------|-----------|--------------------------------------------------|
| id              | INT (PK)  | Identifier                                       |
| eco_id          | INT (FK)  | Reference to the ECO document                    |
| attachment_type | VARCHAR   | Type of attachment (BOM, report, instructions)   |
| file_path       | VARCHAR   | Path or URL to the attached file                 |

---

# 📘 Entity-Relationship (ER) Model

This model represents the relationships between tables in an engineering structure that utilizes Engineering Change Order (ECO) documents.

## 🧱 Main Table: `eco_documents`

Contains core data for the engineering change request.

---

## 🔗 Relationships & Cardinalities

### 🔹 `eco_documents` → `technical_details`
- **Type**: 1:N (One to Many)
- **Description**: One ECO may have multiple technical details.
- **Foreign Key**: `technical_details.eco_id` → `eco_documents.id`

### 🔹 `eco_documents` → `department_actions`
- **Type**: 1:N (One to Many)
- **Description**: One ECO may involve multiple departments with distinct actions.
- **Foreign Key**: `department_actions.eco_id` → `eco_documents.id`

### 🔹 `eco_documents` → `attachments`
- **Type**: 1:N (One to Many)
- **Description**: One ECO may contain multiple attachments.
- **Foreign Key**: `attachments.eco_id` → `eco_documents.id`

---

## 🧠 Simplified Structure Diagram

```text
eco_documents (1)
   ├── technical_details (N)
   ├── department_actions (N)
   └── attachments (N)
```

---


## 📌 Notes on Database Usage:

- All tables are linked via foreign key `eco_id` for consistent tracking and integrity.
- `TEXT` fields are used for flexible-length descriptive entries.
- `BOOLEAN` fields enable logical filtering in dashboards or front-ends.
- This schema is compatible with SQL databases like MySQL, PostgreSQL, SQL Server, and easily adaptable to NoSQL using JSON schemas.
