# ShieldScan Backend Architecture

## 1. Goals

## 2. Architecture Principles

- Modular
- Scalable
- Multi-Tenant
- Extensible
- Queue Driven

---

## 3. Services

Authentication Service

Organization Service

RBAC Service

Asset Service

Discovery Service

Scan Service

Finding Service

Risk Service

Compliance Service

Workflow Service

Dashboard Service

Report Service

Audit Service

Notification Service

---

## 4. Worker Architecture

Discovery Worker

Scan Worker

Normalizer Worker

Risk Worker

Compliance Worker

Report Worker

Notification Worker

---

## 5. Queue Design

Redis

Retry

Dead Letter Queue

Priority Queue

---

## 6. Authentication Flow

Login

Redis Session

Acting-As

Logout

---

## 7. Multi Tenant

Agency

↓

Client

↓

Standalone

---

## 8. Repository Layer

Repository Pattern

RLS

---

## 9. Scan Flow

API

↓

Queue

↓

Worker

↓

Tool Adapter

↓

Engine

---

## 10. PDF Generation

Playwright

React SSR

---

## 11. Audit Logging

---

## 12. Dependency Diagram

---

## 13. Product Vision Integration

Asset Discovery

ASM

Risk

Compliance

Workflow

Internal Scanning

Custom Scan Engine

---

## 14. Phase Evolution

Phase 1

Phase 2

Phase 3

Phase 4

Phase 5
