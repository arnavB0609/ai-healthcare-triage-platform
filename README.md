Healthcare AI-Assisted Triage Platform

Enterprise-Grade, Safety-First, Deterministic Architecture

🚑 Problem Statement

Overcrowded emergency departments and delayed triage decisions can lead to preventable patient harm. Many AI-based healthcare tools rely heavily on generative models for decision-making, raising concerns about safety, hallucinations, and lack of auditability.

This project proposes a deterministic, rule-driven AI-assisted triage platform that uses foundation models strictly for language understanding while preserving clinical decision authority within structured, auditable rule engines aligned with WHO guidelines.

🧠 Solution Overview

The platform enables users to describe symptoms in natural language (text or voice). The system:

Extracts structured clinical signals using Amazon Bedrock (NLP only).

Validates extracted signals through schema-controlled pipelines.

Applies WHO-aligned deterministic triage rules.

Classifies urgency levels (Emergency / Urgent / Non-Urgent).

Provides explainable reasoning and nearby care navigation.

Logs all triage decisions for full auditability.

This ensures:

AI assistance without loss of safety control

Transparent rule-triggered decisions

High-throughput scalable logging

Enterprise-ready architecture

🏗 Architecture Highlights

The system follows a layered architecture:

User Interface Layer – Web/Mobile interface for symptom input

Application Layer – API gateway, session management, validation

AI Processing Layer – Amazon Bedrock for language understanding (non-authoritative)

Clinical Decision Layer (Primary Authority) – Deterministic WHO rule engine

Storage & Logging Layer – Amazon DynamoDB for scalable triage logging

Integration Layer – Emergency escalation & hospital navigation APIs

Foundation models are used only for structured extraction — never for clinical decision authority.

🔧 Technologies Used
AI & Intelligence

Amazon Bedrock (Managed foundation models for NLP)

Schema-constrained structured extraction

Synthetic WHO-aligned triage dataset (600k+ scenarios)

Lightweight ML classifier (Python / scikit-learn)

Backend & Decision Engine

FastAPI (RESTful triage service)

Deterministic WHO rule engine

Hybrid rule + ML urgency classification

Structured signal validation pipeline

AWS Cloud Infrastructure

AWS Bedrock (Managed inference)

AWS Lambda (Serverless hosting)

Amazon DynamoDB (Operational triage logging)

Amazon S3 (Dataset storage & analytics export)

💡 Why This Approach is Safe

Deterministic rule engine retains primary clinical authority

AI models restricted to language understanding only

Structured schema validation prevents hallucinated outputs

Full audit trail maintained via DynamoDB

Serverless cloud-native architecture ensures scalability

📊 Estimated Pilot Infrastructure Cost

Estimated pilot-stage cloud cost:
₹30,000 – ₹1,00,000 per month

Costs scale with usage under a pay-per-request model.
No on-premise hardware required.

Estimates based on projected pilot usage and standard AWS pricing.

📁 Repository Contents

requirements.md – Functional and non-functional requirements

design.md – Detailed system design and architecture explanation

/docs – Architecture diagram and wireframes (if included)

/backend – Application logic (if applicable)

🚀 Deployment Model

Designed for:

Government health systems

Private hospitals

Telemedicine providers

Emergency triage centers

The system supports phased deployment starting from pilot-stage evaluation to enterprise-scale rollout.

⚖️ Disclaimer

This system provides triage assistance and care navigation guidance.
It does not replace professional medical diagnosis or licensed clinical judgment.
