# Project Title
WHO-Aligned AI-Assisted Triage & Care Navigation System

---

## 1. Problem Statement

Healthcare ecosystems often struggle with early-stage symptom interpretation, especially when users provide unstructured, conversational, or multilingual input. This leads to delays in urgency assessment and inefficient pre-hospital decision-making.

The objective of this project is to design a safety-first, AI-assisted triage and care navigation system that improves clarity, efficiency, and structured clinical interpretation — without performing medical diagnosis.

---

## 2. Scope

The system:

- Accepts free-text or voice symptom descriptions
- Converts unstructured input into structured clinical signals
- Applies WHO-aligned deterministic triage logic
- Classifies urgency levels (Emergency / Urgent / Non-Urgent)
- Provides explainable reasoning and care navigation guidance

The system does NOT:

- Provide medical diagnosis
- Replace licensed medical professionals
- Perform autonomous medical decision-making

---

## 3. Functional Requirements

### 3.1 Input Handling
- Accept user symptom input via text or voice
- Support conversational, free-form descriptions
- Normalize input for structured processing

### 3.2 Structured Signal Extraction
- Extract:
  - Symptoms
  - Duration
  - Age group
  - ABC indicators (Airway, Breathing, Circulation)
  - Danger signs
- Validate output using schema-constrained structure

### 3.3 Triage Decision Engine
- Apply WHO-aligned ABC-based rule logic
- Evaluate mental status where applicable
- Trigger danger sign overrides
- Assign urgency classification:
  - Emergency
  - Urgent
  - Non-Urgent

### 3.4 Assistive ML Layer
- Use synthetic dataset-trained classifier
- Reinforce decision boundaries
- Must NOT override rule-based safety logic

### 3.5 Output & Guidance
- Display urgency level clearly
- Provide rule-triggered explanation
- Provide next-step care guidance
- Display safety disclaimer

---

## 4. Non-Functional Requirements

- Deterministic and auditable decision logic
- High availability cloud infrastructure
- Scalable serverless deployment
- Secure logging and audit trail
- No storage of personally identifiable medical data

---

## 5. Data Requirements

- 600,000+ synthetic WHO-aligned triage scenarios
- No real patient records used
- Public clinical logic references only
- Structured synthetic dataset used for ML training

---

## 6. Compliance & Boundaries

- Foundation models used only for language understanding
- Clinical decision authority remains rule-based
- AI operates as assistive layer only
- Designed for responsible deployment within healthcare ecosystems
