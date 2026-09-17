# Page Structure — {Your Project Name}

Space: `{SPACEKEY}`
Prefix: `{PREFIX}`

---

## Sections

| Section | Naming Prefix | Description | Section Owner |
|---------|--------------|-------------|---------------|
| Governance Hub | `{PREFIX}-HUB` | Standards, cross-cutting docs, governance, AI initiative | Documentation Champion |
| Frontend | `{PREFIX}-FRONT` | {frontend technologies}, components, frontend configs | Tech Lead Frontend |
| Backend & Services | `{PREFIX}-BACK` | {backend technologies} | Tech Lead Backend |
| UI/UX Design | `{PREFIX}-DESIGN` | Design system, guidelines, Figma, research | Design Lead |
| Business & Product | `{PREFIX}-BIZ` | Product vision, business rules, features, processes | Product Owner |
| Architecture & Cloud | `{PREFIX}-ARCH` | {cloud and infrastructure} | Solution Architect |
| Security & Compliance | `{PREFIX}-SEC` | Security SDLC, compliance, access, audits | Security Lead |
| QA & Testing | `{PREFIX}-QA` | Testing strategy, test plans, automation, quality metrics | QA Lead |

> **Security**: The "Security & Compliance" root page must have **Page Restrictions** applied. Confluence Cloud inherits restrictions to child pages. Restrict to: security team + architects + tech leads.

---

## Full Page Tree

```
Home ({SPACEKEY} — Welcome page with links to all sections)
│
├── [{PREFIX}-HUB] Governance Hub
│   ├── [{PREFIX}-HUB] Project Overview
│   │   ├── [{PREFIX}-HUB] Project Charter and Objectives
│   │   ├── [{PREFIX}-HUB] Team Directory and Contacts
│   │   ├── [{PREFIX}-HUB] Onboarding Guide
│   │   └── [{PREFIX}-HUB] Glossary
│   ├── [{PREFIX}-HUB] Documentation Standards
│   │   ├── [{PREFIX}-HUB] How to Write Documentation (Style Guide)
│   │   ├── [{PREFIX}-HUB] Naming Conventions
│   │   ├── [{PREFIX}-HUB] Label Taxonomy
│   │   ├── [{PREFIX}-HUB] Template Catalog
│   │   ├── [{PREFIX}-HUB] Decision Guide — What Goes in Confluence
│   │   └── [{PREFIX}-HUB] Document Lifecycle Policy
│   ├── [{PREFIX}-HUB] Cross-Cutting Documentation
│   │   ├── [{PREFIX}-HUB] Global Configurations
│   │   │   ├── [{PREFIX}-HUB] Secrets Management Policy
│   │   │   ├── [{PREFIX}-HUB] Shared Environment Variables
│   │   │   └── [{PREFIX}-HUB] Cross-Component Configuration Map
│   │   ├── [{PREFIX}-HUB] Environment Matrix
│   │   │   ├── [{PREFIX}-HUB] DEV Environment
│   │   │   ├── [{PREFIX}-HUB] QA Environment
│   │   │   ├── [{PREFIX}-HUB] STG Environment
│   │   │   └── [{PREFIX}-HUB] PROD Environment
│   │   ├── [{PREFIX}-HUB] Integration Map
│   │   │   ├── [{PREFIX}-HUB] System-to-System Dependencies
│   │   │   ├── [{PREFIX}-HUB] API Contracts Registry (index)
│   │   │   └── [{PREFIX}-HUB] Data Flow Diagrams
│   │   └── [{PREFIX}-HUB] AS-IS to TO-BE Transition
│   │       ├── [{PREFIX}-HUB] Migration Status Dashboard
│   │       ├── [{PREFIX}-HUB] AS-IS Component Inventory
│   │       └── [{PREFIX}-HUB] TO-BE Component Mapping
│   ├── [{PREFIX}-HUB] Releases and Deployments
│   │   ├── [{PREFIX}-HUB] Release Calendar
│   │   ├── [{PREFIX}-HUB] Release Notes Archive
│   │   │   └── [{PREFIX}-HUB] Release vX.Y.Z
│   │   └── [{PREFIX}-HUB] Deployment Runbooks (index linking to Architecture section)
│   ├── [{PREFIX}-HUB] Governance and Reviews
│   │   ├── [{PREFIX}-HUB] Documentation Review Calendar
│   │   ├── [{PREFIX}-HUB] Quarterly Audit Log
│   │   └── [{PREFIX}-HUB] Change Log (structural changes to the doc system)
│   └── [{PREFIX}-HUB] AI Documentation Initiative
│       ├── [{PREFIX}-HUB] AI Integration Roadmap
│       ├── [{PREFIX}-HUB] Automation Inventory
│       └── [{PREFIX}-HUB] AI-Generated Content Policy
│
├── [{PREFIX}-FRONT] Frontend
│   ├── [{PREFIX}-FRONT] Architecture and Stack
│   │   ├── [{PREFIX}-FRONT] React Application Architecture
│   │   ├── [{PREFIX}-FRONT] WordPress CMS Architecture
│   │   ├── [{PREFIX}-FRONT] Technical Decisions (ADRs)
│   │   └── [{PREFIX}-FRONT] Component Library Reference
│   ├── [{PREFIX}-FRONT] Environment Configuration
│   │   ├── [{PREFIX}-FRONT] Local Development Setup
│   │   ├── [{PREFIX}-FRONT] DEV Environment Config
│   │   ├── [{PREFIX}-FRONT] QA Environment Config
│   │   ├── [{PREFIX}-FRONT] STG Environment Config
│   │   └── [{PREFIX}-FRONT] PROD Environment Config
│   ├── [{PREFIX}-FRONT] Functional Documentation
│   │   ├── [{PREFIX}-FRONT] [Module/Feature Name]
│   │   │   ├── [{PREFIX}-FRONT] Functional Specification
│   │   │   ├── [{PREFIX}-FRONT] AS-IS Flow
│   │   │   ├── [{PREFIX}-FRONT] TO-BE Flow
│   │   │   └── [{PREFIX}-FRONT] Implementation Notes
│   │   └── ... (repeat per module)
│   ├── [{PREFIX}-FRONT] Technical Guides
│   │   ├── [{PREFIX}-FRONT] Build and Deployment Process
│   │   ├── [{PREFIX}-FRONT] Code Standards
│   │   ├── [{PREFIX}-FRONT] Testing Strategy
│   │   ├── [{PREFIX}-FRONT] Performance Guidelines
│   │   ├── [{PREFIX}-FRONT] Accessibility Compliance
│   │   └── [{PREFIX}-FRONT] Analytics Implementation
│   ├── [{PREFIX}-FRONT] Runbooks
│   │   ├── [{PREFIX}-FRONT] Incident Response — Frontend
│   │   └── [{PREFIX}-FRONT] Common Troubleshooting
│   └── [{PREFIX}-FRONT] Knowledge Base
│       ├── [{PREFIX}-FRONT] Decision Log
│       └── [{PREFIX}-FRONT] Lessons Learned
│
├── [{PREFIX}-BACK] Backend & Services
│   ├── [{PREFIX}-BACK] Architecture and Stack
│   │   ├── [{PREFIX}-BACK] Microservices Overview
│   │   ├── [{PREFIX}-BACK] Lambda Functions Catalog
│   │   ├── [{PREFIX}-BACK] API Gateway Configuration
│   │   └── [{PREFIX}-BACK] Technical Decisions (ADRs)
│   ├── [{PREFIX}-BACK] API Documentation
│   │   ├── [{PREFIX}-BACK] [Service Name] API
│   │   │   ├── [{PREFIX}-BACK] API Specification (or link to Swagger/OpenAPI)
│   │   │   ├── [{PREFIX}-BACK] Request-Response Examples
│   │   │   ├── [{PREFIX}-BACK] Error Codes and Handling
│   │   │   └── [{PREFIX}-BACK] Rate Limits and SLAs
│   │   └── ... (repeat per service)
│   ├── [{PREFIX}-BACK] Service Catalog
│   │   ├── [{PREFIX}-BACK] [Service Name]
│   │   │   ├── [{PREFIX}-BACK] Service Overview
│   │   │   ├── [{PREFIX}-BACK] Data Model
│   │   │   ├── [{PREFIX}-BACK] Dependencies and Integrations
│   │   │   ├── [{PREFIX}-BACK] Environment Configuration
│   │   │   └── [{PREFIX}-BACK] Deployment Guide
│   │   └── ... (repeat per service)
│   ├── [{PREFIX}-BACK] Forms Microservices
│   │   ├── [{PREFIX}-BACK] Forms Processing Architecture
│   │   ├── [{PREFIX}-BACK] [Form Name] Specification
│   │   └── [{PREFIX}-BACK] Validation Rules Reference
│   ├── [{PREFIX}-BACK] Functional Documentation
│   │   ├── [{PREFIX}-BACK] [Functional Area]
│   │   │   ├── [{PREFIX}-BACK] Functional Specification
│   │   │   ├── [{PREFIX}-BACK] AS-IS Flow
│   │   │   └── [{PREFIX}-BACK] TO-BE Flow
│   │   └── ...
│   ├── [{PREFIX}-BACK] Runbooks
│   │   ├── [{PREFIX}-BACK] Incident Response — Backend
│   │   └── [{PREFIX}-BACK] Common Troubleshooting
│   └── [{PREFIX}-BACK] Knowledge Base
│       ├── [{PREFIX}-BACK] Decision Log
│       └── [{PREFIX}-BACK] Lessons Learned
│
├── [{PREFIX}-DESIGN] UI/UX Design
│   ├── [{PREFIX}-DESIGN] Design System
│   │   ├── [{PREFIX}-DESIGN] Design Principles
│   │   ├── [{PREFIX}-DESIGN] Brand Guidelines Reference
│   │   ├── [{PREFIX}-DESIGN] Component Pattern Library
│   │   │   ├── [{PREFIX}-DESIGN] [Component Name] — Usage Guide
│   │   │   └── ...
│   │   └── [{PREFIX}-DESIGN] Accessibility Standards
│   ├── [{PREFIX}-DESIGN] Design Deliverables Index
│   │   ├── [{PREFIX}-DESIGN] [Feature/Page Name]
│   │   │   ├── [{PREFIX}-DESIGN] Design Brief
│   │   │   ├── [{PREFIX}-DESIGN] Figma Links and Embeds
│   │   │   ├── [{PREFIX}-DESIGN] Interaction Specifications
│   │   │   └── [{PREFIX}-DESIGN] Design Review Notes
│   │   └── ...
│   ├── [{PREFIX}-DESIGN] User Research
│   │   ├── [{PREFIX}-DESIGN] Research Plan
│   │   ├── [{PREFIX}-DESIGN] Persona Definitions
│   │   ├── [{PREFIX}-DESIGN] Usability Test Results
│   │   └── [{PREFIX}-DESIGN] User Journey Maps
│   └── [{PREFIX}-DESIGN] Knowledge Base
│       ├── [{PREFIX}-DESIGN] Design Decision Log
│       └── [{PREFIX}-DESIGN] Lessons Learned
│
├── [{PREFIX}-BIZ] Business & Product
│   ├── [{PREFIX}-BIZ] Product Vision and Strategy
│   │   ├── [{PREFIX}-BIZ] Product Roadmap (high level)
│   │   ├── [{PREFIX}-BIZ] Business Objectives and KPIs
│   │   └── [{PREFIX}-BIZ] Stakeholder Map
│   ├── [{PREFIX}-BIZ] Business Definitions
│   │   ├── [{PREFIX}-BIZ] Business Process Catalog
│   │   ├── [{PREFIX}-BIZ] Business Rules Reference
│   │   ├── [{PREFIX}-BIZ] Regulatory Requirements
│   │   └── [{PREFIX}-BIZ] Data Dictionary (business terms)
│   ├── [{PREFIX}-BIZ] Feature Documentation
│   │   ├── [{PREFIX}-BIZ] [Epic/Feature Name]
│   │   │   ├── [{PREFIX}-BIZ] Business Context and Requirements
│   │   │   ├── [{PREFIX}-BIZ] User Story Map (link to issue tracker filter)
│   │   │   ├── [{PREFIX}-BIZ] Acceptance Criteria Summary
│   │   │   ├── [{PREFIX}-BIZ] AS-IS Business Process
│   │   │   └── [{PREFIX}-BIZ] TO-BE Business Process
│   │   └── ...
│   ├── [{PREFIX}-BIZ] Analytics and Metrics
│   │   ├── [{PREFIX}-BIZ] Analytics Implementation Guide (GTM, GA4)
│   │   └── [{PREFIX}-BIZ] KPI Dashboard Links
│   └── [{PREFIX}-BIZ] Knowledge Base
│       ├── [{PREFIX}-BIZ] Business Decision Log
│       └── [{PREFIX}-BIZ] Lessons Learned
│
├── [{PREFIX}-ARCH] Architecture & Cloud
│   ├── [{PREFIX}-ARCH] Architecture Overview
│   │   ├── [{PREFIX}-ARCH] Solution Architecture Document (SAD)
│   │   ├── [{PREFIX}-ARCH] High-Level Architecture Diagram
│   │   ├── [{PREFIX}-ARCH] Architecture Decision Records (ADRs)
│   │   │   └── [{PREFIX}-ARCH] ADR-NNNN — [Decision Title]
│   │   └── [{PREFIX}-ARCH] Non-Functional Requirements
│   ├── [{PREFIX}-ARCH] AWS Infrastructure
│   │   ├── [{PREFIX}-ARCH] Account Structure and Organization
│   │   ├── [{PREFIX}-ARCH] Network Architecture (VPC, subnets)
│   │   ├── [{PREFIX}-ARCH] IAM Roles and Policies
│   │   │   ├── [{PREFIX}-ARCH] [Role Name] — Definition and Justification
│   │   │   └── [{PREFIX}-ARCH] Deployment Role Requests
│   │   │       └── [{PREFIX}-ARCH] Role Request — [Description]
│   │   ├── [{PREFIX}-ARCH] AWS Service Catalog
│   │   │   ├── [{PREFIX}-ARCH] CloudFront Configuration
│   │   │   ├── [{PREFIX}-ARCH] S3 Bucket Inventory
│   │   │   ├── [{PREFIX}-ARCH] Lambda Deployment Configuration
│   │   │   ├── [{PREFIX}-ARCH] API Gateway Setup
│   │   │   ├── [{PREFIX}-ARCH] RDS/DynamoDB Configuration
│   │   │   └── ... (per AWS service used)
│   │   └── [{PREFIX}-ARCH] Cost Management and Tagging Strategy
│   ├── [{PREFIX}-ARCH] Infrastructure Requests
│   │   ├── [{PREFIX}-ARCH] Infrastructure Request Process
│   │   ├── [{PREFIX}-ARCH] Request Registry
│   │   │   └── [{PREFIX}-ARCH] Infra Request — [Description]
│   │   └── [{PREFIX}-ARCH] Provisioned Resources Inventory
│   ├── [{PREFIX}-ARCH] Cloud Deployments
│   │   ├── [{PREFIX}-ARCH] CI/CD Pipeline Architecture
│   │   ├── [{PREFIX}-ARCH] Deployment Request Log
│   │   │   └── [{PREFIX}-ARCH] Deployment Request — [Description]
│   │   ├── [{PREFIX}-ARCH] Infrastructure-as-Code Reference
│   │   └── [{PREFIX}-ARCH] Environment Provisioning Guides
│   ├── [{PREFIX}-ARCH] Monitoring and Observability
│   │   ├── [{PREFIX}-ARCH] Monitoring Strategy
│   │   ├── [{PREFIX}-ARCH] Alert Configuration
│   │   ├── [{PREFIX}-ARCH] Logging Architecture
│   │   └── [{PREFIX}-ARCH] Dashboard Links
│   └── [{PREFIX}-ARCH] Knowledge Base
│       ├── [{PREFIX}-ARCH] Architecture Decision Log
│       └── [{PREFIX}-ARCH] Lessons Learned
│
├── [{PREFIX}-SEC] Security & Compliance
│   │
│   │   > **Page Restrictions**: Apply read restriction on this root page.
│   │   > Confluence Cloud inherits restrictions to child pages.
│   │   > Access: security team + architects + tech leads.
│   │
│   ├── [{PREFIX}-SEC] Security SDLC
│   │   ├── [{PREFIX}-SEC] Secure Development Lifecycle Policy
│   │   ├── [{PREFIX}-SEC] Security Requirements Checklist
│   │   ├── [{PREFIX}-SEC] Code Review Checklist (Security)
│   │   └── [{PREFIX}-SEC] Dependency Vulnerability Policy
│   ├── [{PREFIX}-SEC] Cybersecurity Documentation
│   │   ├── [{PREFIX}-SEC] Threat Model
│   │   ├── [{PREFIX}-SEC] Security Architecture
│   │   ├── [{PREFIX}-SEC] Penetration Test Reports
│   │   │   └── [{PREFIX}-SEC] Pen Test — [Scope]
│   │   ├── [{PREFIX}-SEC] Vulnerability Assessment Log
│   │   └── [{PREFIX}-SEC] Security Incident Reports
│   ├── [{PREFIX}-SEC] Compliance and Audit
│   │   ├── [{PREFIX}-SEC] Regulatory Compliance Matrix
│   │   ├── [{PREFIX}-SEC] Audit Trail Documentation
│   │   ├── [{PREFIX}-SEC] Data Privacy (GDPR / Local Regulation)
│   │   └── [{PREFIX}-SEC] Audit Reports Archive
│   ├── [{PREFIX}-SEC] Access Management
│   │   ├── [{PREFIX}-SEC] Role-Based Access Control (RBAC) Matrix
│   │   ├── [{PREFIX}-SEC] Service Account Inventory
│   │   └── [{PREFIX}-SEC] Access Review Calendar
│   └── [{PREFIX}-SEC] Certificates and Renewals
│       ├── [{PREFIX}-SEC] SSL/TLS Certificate Inventory
│       └── [{PREFIX}-SEC] Renewal Calendar
│
└── [{PREFIX}-QA] QA & Testing
    ├── [{PREFIX}-QA] QA Strategy
    │   ├── [{PREFIX}-QA] Overall Testing Strategy
    │   ├── [{PREFIX}-QA] Test Types and Tools
    │   ├── [{PREFIX}-QA] Automation Strategy
    │   └── [{PREFIX}-QA] Quality Criteria and Metrics
    ├── [{PREFIX}-QA] Test Plans
    │   ├── [{PREFIX}-QA] [Feature/Sprint] — Test Plan
    │   └── ... (repeat per test cycle)
    ├── [{PREFIX}-QA] QA Environments
    │   ├── [{PREFIX}-QA] QA Environment Configuration
    │   ├── [{PREFIX}-QA] Test Data and Management
    │   └── [{PREFIX}-QA] Compatibility Matrix (browsers, devices)
    ├── [{PREFIX}-QA] Reports and Metrics
    │   ├── [{PREFIX}-QA] Defect Dashboard (link to issue tracker dashboard)
    │   ├── [{PREFIX}-QA] Test Coverage Reports
    │   └── [{PREFIX}-QA] Quality Retrospectives
    ├── [{PREFIX}-QA] Test Automation
    │   ├── [{PREFIX}-QA] Framework and Tools (Selenium/Cypress/Playwright)
    │   ├── [{PREFIX}-QA] Framework Setup Guide
    │   ├── [{PREFIX}-QA] Automation Coverage (metrics)
    │   └── [{PREFIX}-QA] Automation Technical Decisions (ADRs)
    ├── [{PREFIX}-QA] Guides and Processes
    │   ├── [{PREFIX}-QA] How to Report a Defect (guide for devs)
    │   ├── [{PREFIX}-QA] Regression Process
    │   ├── [{PREFIX}-QA] Pre-Deploy Test Checklist
    │   └── [{PREFIX}-QA] Accessibility Testing Guide
    └── [{PREFIX}-QA] Knowledge Base
        ├── [{PREFIX}-QA] QA Decision Log
        └── [{PREFIX}-QA] Lessons Learned
```

---

## Space Configuration

1. **Home page**: Create with links to all 8 main sections (use Table of Children macro)
2. **Root sections**: Create the 8 first-level pages as parent pages for each frente
3. **Templates**: Configure all 11 templates as Space Templates in {SPACEKEY}
4. **Initial labels**: Add `team:{team}` to each section's root page
5. **Page Restrictions**: Apply read restriction on the "Security & Compliance" root page — Confluence inherits the restriction to all child pages
6. **Sidebar**: Organize shortcuts to the 8 main sections

---

## Migration to Multi-Space (future)

If the project grows and frentes need to be separated into their own spaces:

1. Create the new space in Confluence (e.g., `{PREFIX}-FRONT`)
2. Move the pages from the "Frontend" section to the new space (native Confluence: select page > Move)
3. Titles already have the correct prefix (`[{PREFIX}-FRONT] Func Spec — ...`) — no renaming needed
4. Labels already identify the team (`team:frontend`) — no re-labeling needed
5. Replicate templates as Space Templates in the new space
6. Update permissions: configure Space Permissions instead of Page Restrictions
