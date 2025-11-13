---
title: "Should the Data Organization Sit in IT?"
date: 2025-11-05T18:29:21+01:00
draft: false
author: "David Raoul Maas, GPTS-5"
tags:
  - CTO
  - Data
  - Strategy
  - Management
  - Organization
image: /images/blog_data_org.png
description: ""
toc:
---

## Introduction

Few questions in data leadership spark as much debate as this one:  
**Should the data organization sit in IT, or should it stand on its own?**

At first glance, it sounds like an org-chart detail. In reality, it defines how your company thinks about data: as *infrastructure* or as *a product*.  

I’ve seen both setups and both can work.  
But the placement of the data team deeply shapes its culture, priorities, and even its speed.  
And while many companies instinctively tuck data under IT, that’s often more out of legacy convenience than strategic clarity.

Let’s unpack what really drives this decision and when it might be time to move your data team out of IT’s basement.

---

## 1. Purpose and Maturity

The first question is simple but revealing:  
**What is your data team actually responsible for?**

--> If your main goal is **reliable pipelines, stable infrastructure, and compliance**, then IT alignment makes sense. IT already knows how to run systems, standardize tools, and manage SLAs.

--> But if your team’s mission is **insights, enablement, and data products**, the IT framing quickly becomes a bottleneck. Data becomes less about tickets and uptime and more about discovery and iteration.

In early-stage companies, data often starts close to product or finance. It’s lightweight, business-driven, and fast. Over time, as complexity grows, someone inevitably says: *“We need to formalize this - let’s move it under IT.”*  

That’s when data starts to slow down.

**Rule of thumb:**  
The more your data team drives business value, the less it belongs in IT.

---

## 2. Ownership of Outcomes

Here’s where many orgs stumble.  
IT typically owns systems, not outcomes. Their mandate is uptime, security, and efficiency and not whether marketing understands customer churn. I've met IT guys that don't even know what customer churn means.

If your data team sits in IT, it risks becoming a **service center**:  
- “Can you build me a report?”  
- “Can you add this new data source?”  

If your data team sits closer to business or product, it becomes an **enabler**:  
- “How can we measure this experiment?”  
- “What’s the driver behind this drop in conversion?”  

Both models deliver data, but only one delivers insight.  
And if you’re trying to make data part of your decision-making culture, you need ownership aligned with business outcomes, not just system health.

---

## 3. Speed vs. Standardization

This is the most visible tension.

| Factor | Data in IT | Data Outside IT |
|--------|-------------|----------------|
| **Speed of delivery** | Slower (process-heavy) | Faster (closer to decision-makers) |
| **Standardization** | Strong (central control) | Risk of duplication |
| **Governance** | Built-in | Needs explicit effort |
| **Innovation** | Conservative | Experimental |

Neither is “better”, they’re optimized for different things.  
If you’re a bank, IT’s rigor is an advantage.  
If you’re a startup, it’s an anchor.

The trick is not to pick one forever, but to **evolve**:  
- Early phase → under IT for structure and compliance  
- Growth phase → hybrid model for agility  
- Mature phase → federated ownership under a CDO or domain structure

---

## 4. Talent and Culture

Where your data org lives determines the kind of people it attracts.

In IT, you get system thinkers, reliable, process-driven engineers.  
Outside IT, you attract product thinkers, curious, business-fluent problem solvers.

Both are valuable, but mixing them under the wrong leadership can create cultural friction.  
You can’t tell someone measured on SLA uptime to “experiment fast.”  
And you can’t tell a data analyst embedded in product to “raise a Jira ticket to add a table.”

If your goal is to bridge technical depth with business impact, data probably needs its own leadership and cultural space.

---

## 5. Governance and Security

To be fair: IT brings something irreplaceable: **governance discipline**.

Security, compliance, access control, and auditability are not things business-led teams typically enjoy maintaining.  
If your industry is regulated (finance, health, energy), you absolutely need IT’s rigor.  

But that doesn’t mean IT has to *own* all of data — just the guardrails.  
A common (and healthy) model is:
- **Data platform and infrastructure in IT**
- **Analytics and modeling in the business**
  
That keeps governance centralized but lets insights flow freely.

---

## 6. Company Size and Stage

There’s a natural lifecycle to where data belongs.

| Stage | Typical Setup | Rationale |
|--------|----------------|-----------|
| **Early-stage (0-100 people)** | A few analysts under Product or Finance | Speed and flexibility matter most |
| **Growth (100-1000)** | Hybrid: IT owns platform, business owns analytics | Balance structure with agility |
| **Enterprise (1000+)** | Federated model with a CDO | Scale and governance dominate |

Most teams move through these phases whether they plan to or not.  
The key is to notice when your current setup starts to create friction and adjust before your org calcifies.

---

## 7. The Rise of Hybrid Models

More and more companies are landing on **hybrid data organizations**:

--> **Data Platform in IT**  
  Focused on infrastructure, reliability, and governance.  

--> **Data Products in Business Units**  
  Focused on insight generation, experimentation, and value delivery.  

--> **Central Data Leadership (CDO or Head of Data)**  
  Bridges both sides, sets standards, and aligns priorities.

This model accepts the obvious truth:  
Data isn’t purely a technical or business concern. It’s both.  
The goal isn’t ownership. It’s *alignment*.

---

## Argue About Purpose

Whether your data organization sits in IT or elsewhere is ultimately secondary.  
What really matters is **clarity of purpose** and **alignment of incentives**.

If your goal is reliability and compliance, IT is the right home.  
If your goal is experimentation, enablement, and business insight, give data its own leadership seat — or at least let it breathe outside IT’s process machinery.

Personally, I’ve seen small teams move *much* faster once they stopped treating data as infrastructure and started treating it as a product.  
And ironically, the more independent the data org became, the better its collaboration with IT got. Because the boundaries were finally clear.

**Where data sits matters less than what it’s accountable for.**  
Decide that first, the org chart will follow.

