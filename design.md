# System Design Document
WHO-Aligned AI-Assisted Triage & Care Navigation System

---

## 1. Architecture Overview

The system follows a layered, safety-first architecture separating language understanding from clinical decision authority.

High-Level Layers:

1. User Interface Layer
2. Application Layer
3. AI Processing Layer
4. Clinical Decision Layer (Primary Authority)
5. Storage & Logging Layer
6. Integration Layer

---

## 2. User Interface Layer

- Web / Mobile Interface
- Text and voice symptom input
- Structured urgency display
- Care navigation recommendations
- Safety disclaimers

---

## 3. Application Layer

- API Gateway
- Session Management
- Input Validation Module
- Structured signal validation pipeline

---

## 4. AI Processing Layer

Technology: Amazon Bedrock (Foundation Models)

Responsibilities:

- Normalize multilingual or conversational input
- Extract structured clinical signals
- Output schema-validated structured data

Important Constraint:

Foundation models are used ONLY for language understanding and structured extraction — NOT for clinical decision-making.

---

## 5. Clinical Decision Layer (Primary Authority)

Components:

- WHO-aligned deterministic rule engine
- ABC logic framework
- Danger sign override system
- Deterministic urgency classification
- Assistive ML classifier (non-authoritative)

Decision authority remains fully rule-constrained.

---

## 6. Storage & Logging Layer

- Amazon DynamoDB for operational triage records
- Decision logging and audit trail
- Model interaction logging
- Structured case database

This supports scalability, auditability, and high-throughput logging.

---

## 7. Integration Layer

- Emergency service escalation interface
- Hospital / Care navigation API
- Reporting dashboard (optional future enhancement)

---

## 8. Technology Stack

AI Layer:
- Amazon Bedrock
- Synthetic WHO-aligned dataset
- Python (ML classifier)

Backend:
- FastAPI (RESTful triage service)
- Hybrid Rule + ML urgency classification

Cloud Infrastructure:
- AWS Lambda (Application Hosting)
- Amazon DynamoDB (Operational logging)
- Amazon S3 (Dataset storage & analytics export)

---

## 9. Safety Architecture Principles

- Deterministic clinical authority
- Assistive ML boundary enforcement
- No diagnosis generation
- Structured audit logging
- Responsible AI deployment within healthcare ecosystems
