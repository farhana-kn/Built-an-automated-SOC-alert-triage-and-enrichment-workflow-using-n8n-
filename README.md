SOC Alert Triage & Enrichment Automation (n8n)

📌 Project Overview

This project demonstrates a Security Orchestration, Automation, and Response (SOAR)–style workflow built using n8n.
It simulates how modern Security Operations Centers (SOCs) automate alert ingestion, enrichment, prioritization, and escalation to reduce analyst workload and alert fatigue.

The system ingests alerts via webhooks, enriches contextual data using external APIs, applies risk-based decision logic, and notifies analysts automatically — closely mirroring real-world SOC pipelines.

⚙️ Architecture Flow

     Webhook Trigger,
   → Data Normalization,
   → IP Geo Enrichment,
   → Dynamic Risk Scoring,
   → Conditional Severity-Based Escalation,
   → Analyst Notification,
   → Error Handling Workflow
   
🔐 Key Features

Webhook-based Alert Ingestion,
Simulates SIEM → SOAR alert forwarding,
Alert Normalization,
Standardizes incoming JSON fields for consistent processing,
IP Enrichment,
Fetches geo-location, ISP, and context using external IP intelligence APIs,
Dynamic Risk Scoring Engine,

Calculates alert risk score based on:
Alert severity,
Geo-location of source IP,
Conditional Decision Logic,
Routes alerts based on risk and severity thresholds,
Severity-Based Escalation,
High-risk alerts trigger analyst notifications,
Low-risk alerts are logged or ignored,
Automated Analyst Notifications,
Sends actionable alerts via Email (Slack/Teams extensible),
Workflow-Level Error Handling,
Dedicated error workflow ensures failures are logged and notified

🎯 Operational Value

Reduces manual alert triage effort,
Improves prioritization accuracy using contextual data,
Demonstrates risk-based SOC decision making,
Minimizes alert fatigue,
Reflects real-world SOAR design patterns

🧠 Learning Outcomes

Translating SOC workflows into automation logic,
Designing dynamic risk scoring models,
Implementing enrichment-driven alert triage,
Building resilient automation with error handling,
Understanding SOAR architecture fundamentals

🧪 Sample Alert Structure
{
  "alert_name": "Failed Login",
  "severity": "High",
  "source_ip": "8.8.8.8",
  "country": "United States",
  "city": "Ashburn",
  "isp": "Google LLC",
  "risk_score": 50,
  "timestamp": "America/New_York"
}

🛠 Technologies Used

n8n – Workflow automation / SOAR simulation,
HTTP APIs – IP enrichment & threat intelligence,
JSON – Alert processing format,
Email / Notification Services,

📌 Use Cases

SOC alert triage automation,
SOAR workflow prototyping,
Cybersecurity training & labs,
Automation-driven incident response simulations,

🚀 Future Enhancements

Integration with SIEM platforms (Splunk, Elastic),
Threat reputation scoring (VirusTotal, AbuseIPDB),
Automated response actions (IP blocking, ticket creation),
Dashboard visualization of alert trends
