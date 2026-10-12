# Portfolio Materials

Reusable copy for presenting the AI Lead Qualification System. The descriptions below reflect the implemented repository and do not claim production usage or client results.

## LinkedIn — English

I built an AI Lead Qualification System with n8n, Google Gemini, Google Sheets, and Gmail. The workflow validates and deduplicates inbound leads, combines deterministic business rules with structured AI evaluation, classifies each opportunity as HOT, WARM, or COLD, stores the result in a lightweight CRM, and sends a personalized follow-up. A dedicated error workflow logs failed executions and sends an administrative alert. This portfolio project demonstrates workflow architecture, API integration, structured LLM outputs, security-conscious credential handling, and end-to-end business automation.

## LinkedIn — Spanish

Construí un sistema de calificación de leads con IA utilizando n8n, Google Gemini, Google Sheets y Gmail. El workflow valida y elimina duplicados, combina reglas determinísticas con una evaluación estructurada de IA, clasifica cada oportunidad como HOT, WARM o COLD, guarda el resultado en un CRM ligero y envía un seguimiento personalizado. Un workflow independiente registra errores y envía alertas administrativas. Este proyecto demuestra arquitectura de automatización, integración de APIs, salidas estructuradas de LLM y manejo seguro de credenciales.

## Upwork Project Description

### AI-Powered Lead Qualification and Follow-up Automation

This project demonstrates an end-to-end lead-processing system built with n8n. It receives inbound lead data through an authenticated webhook, validates required fields, prevents duplicate processing, and combines rule-based scoring with Google Gemini analysis.

The workflow produces a deterministic final score, classifies leads as HOT, WARM, or COLD, stores qualification data in Google Sheets, sends a personalized Gmail follow-up, and updates the lead status. A separate error-handling workflow logs failed executions and sends an administrative alert.

The same architecture can be adapted to a client's forms, qualification rules, CRM, email provider, and sales process. It is suitable for businesses that want faster lead response, consistent prioritization, and less manual qualification work.

## CV Bullets

- Designed a 27-node n8n lead-qualification workflow integrating authenticated webhooks, Google Gemini, Google Sheets, and Gmail.
- Implemented hybrid scoring that combines deterministic budget and timeline rules with structured AI evaluation of qualitative buying signals.
- Built validation and duplicate-protection branches that stop invalid or existing leads before costly downstream AI processing.
- Automated HOT, WARM, and COLD routing, personalized email follow-up, and post-send CRM status updates.
- Created a dedicated error workflow that normalizes failures, logs structured execution data, and sends administrative alerts.

## Service Packages

### Basic Lead Automation

- Lead capture from one form or webhook
- Input normalization and validation
- Duplicate detection
- Google Sheets or equivalent lightweight storage
- Basic operational documentation

### AI Lead Qualification

- Everything in Basic Lead Automation
- Client-specific deterministic scoring rules
- Structured AI assessment of qualitative lead signals
- HOT, WARM, and COLD classification
- Qualification summary and recommended action
- Test scenarios for valid, invalid, duplicate, and classification outcomes

### Full Lead Qualification + CRM + Follow-up

- Everything in AI Lead Qualification
- CRM or sales-pipeline integration
- Classification-based personalized email follow-up
- Lead-status updates after successful contact
- Error logging and administrative alerts
- Deployment, credential configuration, handover documentation, and recorded walkthrough

Final scope should be adjusted to the client's form, CRM, qualification rules, integrations, security requirements, and expected lead volume.

## Loom Demo Script — 2–3 Minutes

### 0:00–0:20 — Introduction

"Hi, I'm Omar Hernandez Rojas. This is an AI-powered lead qualification and follow-up system that I built with n8n, Google Gemini, Google Sheets, and Gmail. It automates the process from inbound lead capture to scoring, CRM storage, and personalized follow-up."

### 0:20–0:45 — Business Problem

"Sales teams often review inbound leads manually. That creates delays, inconsistent prioritization, duplicate processing, and repetitive follow-up work. This system applies the same qualification process to every lead while keeping the final score and routing logic auditable."

### 0:45–1:35 — Main Workflow

"The workflow starts with a Header Auth-protected webhook. It normalizes the payload, validates the required fields, and checks the lead's email against the CRM. Invalid and duplicate leads are handled through separate branches before any AI call is made.

For a new valid lead, n8n calculates objective Budget and Timeline points. Google Gemini evaluates only the qualitative signals: Business Need, Company Fit, and Buying Intent. A Structured Output Parser enforces the expected response schema. n8n then calculates the final score and assigns the HOT, WARM, or COLD classification."

### 1:35–2:05 — CRM and Follow-up

"The qualified lead is stored in Google Sheets with the deterministic scores, AI analysis, final classification, and recommended action. The classification router selects the appropriate Gmail message. After a successful send, the CRM row is updated to Contacted and Email Sent equals Yes."

### 2:05–2:30 — Reliability and Security

"A dedicated error workflow captures failed executions, formats the error data, logs it in a separate sheet, and sends an administrative alert. The portfolio exports are sanitized: credentials, API keys, private spreadsheet IDs, and personal email addresses are not included."

### 2:30–2:50 — Closing

"This architecture can be adapted to a company's own forms, qualification rules, CRM, email provider, and sales process. The repository includes the sanitized workflows, architecture documentation, screenshots, setup steps, and security notes."
