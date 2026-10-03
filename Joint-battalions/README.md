# Buildathon Resources

This repository contains the official resources required for the **HireD Buildathon**. Teams should use these documents as the primary reference throughout the Buildathon.

---

## 📁 Repository Structure

```text
Joint-battalions/
│
├── docs/
│   ├── buildathon_guidelines_and_criteria.md
│   ├── hire_d_prd_doc.md
│   └── hire_d_technical_guidelines.md
│
├── assets/
│   ├── logo.png
│   └── logo.svg
│
└── README.md
```

---

## Resources

### 1. Buildathon Guidelines & Criteria

**File:** `docs/buildathon_guidelines_and_criteria.md`

Contains the official Buildathon rules and evaluation guidelines, including:

- Buildathon overview
- Team structure
- Team size requirements
- Technology stack guidelines
- Mandatory SQL database requirement
- Database design submission requirements
- Buildathon phases
- Evaluation criteria
- Documentation requirements
- Security requirements
- Final presentation requirements
- Important expectations

---

### 2. Product Requirements Document

**File:** `docs/hire_d_prd_doc.md`

This is the **Product Requirements Document (PRD)** for the HireD project.

It defines:

- Product vision
- Problem statement
- User roles
- Product scope
- Functional requirements
- End-to-end workflows
- Admin Portal requirements
- B2B Portal requirements
- Driver App requirements
- Payroll and wallet rules
- Invoice and verification flow
- Reports
- High-level data model
- Non-functional requirements
- Assumptions and risks
- Release readiness criteria

> **The PRD defines what needs to be built.**

Teams should carefully understand the PRD before starting implementation.

---

### 3. Technical Guidelines

**File:** `docs/hire_d_technical_guidelines.md`

Contains the technical implementation standards that teams are expected to follow.

This includes:

- Modular Monolithic backend architecture
- SQL database requirement
- Repository structure
- UI and branding guidelines
- Backend module structure
- API guidelines
- Database guidelines
- Naming conventions
- Function and code-quality standards
- Authentication and authorization
- Security guidelines
- File upload security
- Environment configuration
- Logging and audit logging
- Testing guidelines
- Git conventions
- Documentation requirements
- Deployment guidelines
- Final technical checklist

> **The Technical Guidelines define how the product should be built.**

---

## Branding Assets

The repository contains the official HireD branding assets:

```text
assets/logo.png
assets/logo.svg
```

Teams should use the provided logo when implementing:

- Admin Portal
- B2B Portal
- Driver App

Do not replace the provided logo with a custom logo.

---

# Recommended Development Process

Teams should follow this general development flow:

```text
Understand PRD
      ↓
Understand Workflows
      ↓
Design Database
      ↓
Define Architecture
      ↓
Implement Backend
      ↓
Implement Web & Mobile Applications
      ↓
Integrate
      ↓
Test & Secure
      ↓
Document
      ↓
Fix Bugs
      ↓
Deploy
      ↓
Final Demonstration
```

---

## ⚠️ Important

Before starting development, every team should make sure they understand:

1. The **Buildathon Guidelines & Criteria**
2. The **HireD PRD**
3. The **Technical Guidelines**

The PRD is the primary source for **product requirements**, while the Technical Guidelines define the required **technical implementation standards**.

The database design must be prepared and submitted within the **first 2 days of the Buildathon**.

---

## Design Reference

The Admin Portal design reference is:

**HireD Admin Portal:**

https://id-preview--29526d21-889b-410d-affc-7d0297827ba6.lovable.app/

The colour theme and overall visual identity should be consistently applied across:

- Admin Portal
- B2B Portal
- Driver App

---

## Core Technical Requirements

| Area | Requirement |
|---|---|
| Backend | **Modular Monolithic Architecture** |
| Primary Database | **SQL / Relational Database** |
| Admin | Web Application |
| B2B | Web Application |
| Driver | Mobile Application |
| Database Design | Submit within first 2 days |
| Branding | Use provided HireD logo |
| UI Theme | Follow provided design/theme |
| Documentation | Required throughout development |
| Security | Required |
| Testing | Required |
| Version Control | Git required |

---

## Source of Truth

When making implementation decisions, use the following documents:

### Product Requirements

**`docs/hire_d_prd_doc.md`**

Defines **what the system must do**.

### Technical Requirements

**`docs/hire_d_technical_guidelines.md`**

Defines **how the system should be implemented**.

### Buildathon Rules

**`docs/buildathon_guidelines_and_criteria.md`**

Defines the **Buildathon rules, expectations, evaluation, and submission requirements**.

---

## Product Workflow

The core HireD workflow is:

```text
B2B Order
    ↓
Admin Accept / Reject
    ↓
Trip Created
    ↓
Driver Assignment
    ↓
Trip Start
    ↓
Expenses
    ↓
OTP Trip Close
    ↓
Trip Report
    ↓
Driver Payout
    ↓
Month-End Statement
    ↓
Two-Person Verification
    ↓
B2B Partner Access
```

Teams should ensure that the complete workflow works correctly rather than implementing isolated features.

---

## Buildathon Goal

The objective is to take the provided HireD requirements and transform them into a:

> **Complete, functional, secure, maintainable, and documented software product.**

The focus should be on:

```text
PRD Understanding
        ↓
Database Design
        ↓
Architecture
        ↓
Implementation
        ↓
Integration
        ↓
Testing
        ↓
Security
        ↓
Documentation
        ↓
Bug Fixing
        ↓
Final Demonstration
```

---

## Final Reminder

### The PRD defines:

**WHAT to build**

### The Technical Guidelines define:

**HOW to build it**

### The Buildathon Guidelines define:

**WHAT IS EXPECTED FROM THE TEAM**

Teams are expected to understand all three documents before and throughout the implementation process.
