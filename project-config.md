# Project Configuration — Acme Corp Web Portal

> Example configuration. Copy `project-config-template.md` and adapt to your project.

---

## Identity

| Field | Value |
|-------|-------|
| Project name | Acme Corp Web Portal |
| Organization | Acme Corp |
| Naming prefix | ACME |
| Confluence space key | ACMEWEB |
| Confluence URL | https://acme-corp.atlassian.net/wiki |
| Documentation language | english |
| Team size | 5-15 |

## Frentes (Sections)

| Front | Suffix | Technologies | Section Owner | Team Label |
|-------|--------|-------------|---------------|------------|
| Frontend | FRONT | React, WordPress CMS | Tech Lead Frontend | team:frontend |
| Backend | BACK | Microservices, AWS Lambda, API Gateway | Tech Lead Backend | team:backend |
| UI/UX | DESIGN | Figma, Design System | Design Lead | team:design |
| Business | BIZ | Jira, Business Rules | Product Owner | team:business |
| Architecture | ARCH | AWS (CloudFront, S3, Lambda, RDS, IAM) | Solution Architect | team:architecture |
| Security | SEC | SDLC, Compliance, RBAC | Security Lead | team:security |
| QA & Testing | QA | Jira native, Excel (future: Xray/Zephyr) | QA Lead | team:qa |

## Technology Labels

| Label | Description |
|-------|-------------|
| tech:react | Frontend framework |
| tech:wordpress | CMS |
| tech:aws-lambda | Serverless compute |
| tech:api-gateway | API management |
| tech:s3 | Object storage |
| tech:cloudfront | CDN |
| tech:dynamodb | NoSQL database |
| tech:rds | Relational database |
| tech:gtm | Google Tag Manager |
| tech:ga4 | Google Analytics 4 |

## Secrets Platform

| Field | Value |
|-------|-------|
| Tool | AWS Secrets Manager |
| Reference format in docs | See AWS Secrets Manager: {path} |

## Tools

| Tool | Purpose |
|------|---------|
| Jira | Task management and backlog |
| Figma | UI/UX design |
| GitHub | Source code |
| draw.io | Architecture and flow diagrams |
| Swagger/OpenAPI | API documentation |

## Overrides

None.
