# 🤖 AI-Powered Lead Qualification, Research & Outreach Automation

> From decades of manual outreach to an autonomous AI sales assistant — built by a sales leader who lived the problem.

---

## 🧭 Why I Built This

With 6 years of experience across **sales, business development, and revenue leadership roles** — including 3+ years in **Sales leadership and strategy**, I’ve spent thousands of hours watching talented teams get buried under:

- repetitive qualification calls
- scattered CRM notes
- manual outreach copy-paste
- forgotten follow-ups and missed timing

This project was born out of that frustration — but also opportunity.

I wanted to **build something that represents the future of sales**:  
> A hands-off AI system that can score leads, research them online, personalize outreach, and even hit “Send” — while your team focuses on closing.

---

## ⚙️ What This System Does

This is a fully automated, end-to-end **lead enrichment, scoring, and email outreach engine** — no manual work required.

### 💼 What It Handles:

- Captures new leads in Google Sheets (demo layer)
- Uses AI to **score and qualify** each lead (Agent 1)
- Researches company data using the web (Agent 2)
- Personalizes outreach with pain points and positioning (Agent 2)
- Generates a professional cold email (Agent 3)
- Automatically sends the email via Gmail

---

## 🧠 The AI Agent Stack

| Agent | Role | Output |
|-------|------|--------|
| **Agent 1** | Qualifier & Scorer | JSON: qualified, score, industry, insight |
| **Agent 2** | Researcher + Outreach Hook | JSON: company summary, pain points, opportunities, persona |
| **Agent 3** | Email Writer | JSON: subject + short personalized cold email |

Each agent uses:
- 🔎 **Web Search Tool** (Serper.dev) to find live company data
- 🌐 **HTTP Tool** to pull `/about` page content
- 🧠 **Structured Output Parsing** to ensure predictable automation

---

## 🧩 Tech Stack Used

- [x] **n8n** (workflow orchestration + agent routing)
- [x] **OpenRouter GPT-4o Search Preview model, claude 3.5 for writing and GPT-4o mini for logical processing**
- [x] **Serper.dev API** for domain discovery
- [x] **Google Sheets** for simplified data handling
- [x] **Gmail API** for sending final outreach emails

> ⚠️ Google Sheets was used for accessibility and demo clarity — this can easily be adapted to **Airtable, HubSpot, Salesforce, Supabase, or Postgres** depending on your tech stack.
> ⚠️ This completely customizable and every aspect of it can be fine tuned you are requirments.
---

## 💌 Example Final Output

```json
{
  "subject": "Quick question about EcoSolar.vaha's customer response times",
  "email_body": "Ankit, I noticed EcoSolar.vaha's growing momentum in the solar space, and I wondered if you're facing the common challenge of managing increasing customer    inquiries while maintaining quick response times?
   We've helped solar companies reduce their customer response time by 73% through intelligent workflow automation, while simultaneously increasing qualified leads by 45%.    Would you be open to a brief chat about how we could streamline your CRM integration and automate customer service processes to accelerate EcoSolar.vaha's growth?"
}
```

## 🔮 What More Can Be Done

Here’s what this system can evolve into — and how it can support real sales teams at scale:

### 🚀 Enhancement Ideas:
- Swap Google Sheets for Airtable/HubSpot/Notion CRM
- Add phone number/email enrichment via APIs like:
  *Clearbit
  *Apollo
  *PeopleDataLabs
  *Clay.com (proxy to multiple enrichment stacks)
- Add Intent-based Lead Scoring using G2/LinkedIn Signals
- Track email opens, clicks, and replies to trigger follow-ups
- Plug into Slack or Notion for lead alerts or summaries
- Build a lead dashboard in Supabase or Metabase
- Add Zapier triggers to push deals into your pipeline
