# ShieldScan — PROJECT_MASTER_SUMMARY

## Purpose

This document is the single source of truth for the ShieldScan project.

Every future AI session must read this document before making any changes.

Approved decisions must never be redesigned unless a new Architecture Decision Record (ADR) explicitly replaces them.

---

# Project

Name:
ShieldScan

Type:
Multi-Tenant Cybersecurity SaaS Platform

Target Customers:

* VAPT Providers
* MSSPs
* Cybersecurity Consultancies
* Managed Security Providers

---

# Product Vision

ShieldScan is NOT another vulnerability scanner.

ShieldScan is a complete cybersecurity operations platform that enables security companies to manage:

* Clients
* Assets
* Scans
* Findings
* Reports
* Risk
* Remediation
* Teams

from one unified platform.

---

# Product Roadmap

## Phase 1

Core Platform

* Multi-Tenant
* RBAC
* Acting-As
* Client Management
* Team Management
* Asset Discovery
* Scan Management
* Findings
* Reports

Uses external engines:

* Nuclei
* Amass
* Subfinder
* httpx
* Naabu

---

## Phase 2

Risk Platform

* Risk Prioritization
* Compliance Mapping
* Remediation Tracking
* SLA Tracking

---

## Phase 3

Attack Surface Management

Continuous Discovery

Internet-facing Assets

Shadow IT Detection

---

## Phase 4

Internal Security

* Active Directory
* Internal Networks
* Windows Servers
* VLAN Discovery

---

## Phase 5

ShieldScan Engine

Replace external scanners with proprietary engines.

* Discovery Engine
* Vulnerability Engine
* Risk Engine

Add AI-assisted Risk Analysis.

---

# Locked Architecture

The following architecture is frozen.

Never redesign without a formal ADR.

* Multi-Tenant Model
* Authentication
* RBAC
* Acting-As
* Billing Model
* Row Level Security
* Session Model
* Reporting Architecture
* Audit Logging

---

# Current Project Status

Current Phase:

Backend Architecture Complete

Frontend Architecture Not Started

Next Required Artifact:

Frontend Architecture Design

After That:

* Implementation Plan
* Sprint Plan
* Development

---

# Repository Documents

Always read these files before generating new work.

1. ARCHITECTURE_FREEZE_V1.md

2. docs/ADR.md

3. docs/CONTEXT_FOR_AI.md

4. docs/PROJECT_STATUS.md

5. docs/shieldscan-backend-architecture.md

6. docs/shieldscan-database-schema.md

7. docs/shieldscan-api-specification.md

8. docs/shieldscan-vision-schema-extensions.md

---

# AI Instructions

Before doing any work:

1. Read this document completely.

2. Read every referenced document.

3. Continue from the latest project state.

4. Never redesign approved architecture.

5. Never replace existing decisions.

6. Extend the platform instead of rewriting it.

7. If a new architecture decision is required:

* Flag it explicitly.
* Explain why.
* Wait for approval.

Never silently introduce architectural changes.

---

# Current Goal

Continue from Backend Architecture.

Next deliverable:

Frontend Architecture Design

After approval:

Implementation Plan

Sprint Plan

Development

---

Last Updated

June 2026
