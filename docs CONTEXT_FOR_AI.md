# ShieldScan — AI Context File

## Project Overview

### Project Name

ShieldScan

### Project Type

Multi-tenant Cybersecurity SaaS Platform

### Vision

Provide automated cybersecurity posture assessment for organizations through domain, infrastructure, DNS, SSL, email security, technology exposure, reputation, and performance analysis.

### Target Customers

* Individual businesses
* Agencies managing multiple clients
* Enterprise organizations

### Core Value Proposition

A white-label cybersecurity assessment platform allowing agencies and businesses to continuously monitor and improve their external security posture.

---

# Current Project Status

## Current Phase

Architecture & Product Design

## Overall Progress

55%

## Last Completed Document

Finding Type Registry (Canonical Final Edition)

## Current Task

PDF Report Generation Design

## Next Tasks

1. PDF Report Generation Design
2. Cross-Document Consistency Review
3. High-Fidelity Screens
4. Design System
5. Frontend Architecture
6. Backend Architecture
7. Database Implementation
8. API Implementation
9. Frontend Development
10. Testing
11. Deployment

---

# Architecture Decisions (Binding)

## Multi-Tenant Model

Organization Types:

### Agency

Can manage multiple client organizations.

### Client

Belongs to a parent agency.

### Standalone Organization

Independent customer organization.

Rule:

Client organizations MUST have parent_org_id.

---

## Acting-As System

Agency Admins may temporarily act as a client organization.

Rules:

* Session stores homeOrgId.
* Session may contain actingAsOrgId.
* Acting-As expires after 30 minutes.
* Effective organization is computed dynamically.
* Every action is audit logged.

---

## Billing Model

Billing belongs to:

* Agency
* Standalone organization

Client organizations never own subscriptions.

Billing entitlement resolution:

Client Org
→ Parent Agency
→ Subscription

---

## Security Model

### RLS

PostgreSQL Row Level Security enabled.

### Tenant Isolation

Single-org isolation for all tenant data.

Exceptions:

* Subscription
* UsageCounter

These support parent-org billing resolution.

---

## Authentication

Web App:

* Redis session storage
* HttpOnly cookies
* MFA support

API:

* API Key authentication
* Scoped permissions

---

# Completed Documents

## Product & Planning

* PRD
* User Flows
* State & UX Patterns

## Architecture

* Software Architecture
* Component Architecture
* API Design
* Authentication & Authorization Design

## Security

* RBAC Matrix
* MFA Design
* Tenant Isolation Design

## Database

* Prisma Schema Design
* Schema Hardening
* Migration Strategy

## Platform Features

* Monitoring & Alerting Design
* Finding Type Registry

---

# Canonical Finding Registry

Current Status:
43 Finding Types

Modules:

1. SSL
2. Headers
3. DNS
4. WHOIS
5. Technology Detection
6. Email Security
7. Ports
8. Malware/Reputation
9. Lighthouse

Informational-only findings:

* recent_registrar_change
* missing_bimi

These MUST NOT affect score calculations.

---

# Important Constraints

## Never Change

* Organization hierarchy model
* Billing walk-up logic
* Acting-As model
* RBAC capability system
* Finding Type slugs

Breaking these requires a formal ADR.

---

# Open Items

## Pending Decisions

* PDF Report Generation Design
* Final Consistency Review
* High Fidelity Screens

---

# Repository Structure

docs/
├── PRD.md
├── USER_FLOWS.md
├── STATE_UX_PATTERNS.md
├── SOFTWARE_ARCHITECTURE.md
├── COMPONENT_ARCHITECTURE.md
├── API_DESIGN.md
├── DATABASE_SCHEMA.md
├── MIGRATION_STRATEGY.md
├── RBAC.md
├── AUTHORIZATION.md
├── MONITORING_ALERTING.md
├── FINDING_TYPE_REGISTRY.md
├── PDF_REPORT_GENERATION.md
├── ADR.md
├── PROJECT_STATUS.md
└── CONTEXT_FOR_AI.md

---

# Instructions For Future AI Assistants

Before generating new work:

1. Read CONTEXT_FOR_AI.md
2. Read PROJECT_STATUS.md
3. Read all completed architecture documents
4. Continue from Current Task
5. Do NOT redesign previously approved architecture
6. Prefer extending existing decisions over replacing them
7. Maintain backward compatibility with prior documents

Current continuation point:

PDF Report Generation Design
