---
title: "Data Architecture and the Real Total Cost of Ownership: Why “Make or Buy” Is Harder Than It Looks"
date: 2025-11-05T16:29:21+01:00
draft: false
author: "David Raoul Maas, GPTS-5"
tags:
  - CTO
  - Data
  - Strategy
  - Management
  - SaaS
  - Cloud
image: /images/blog_tco_iceberg.png
description: "This blog post tries to emphasize why value-driven decision making should matter."
toc:
---

## Introduction

Every leadership team faces the same strategic dilemma sooner or later:  
**Should we build our own data stack, or should we buy into managed solutions?**

On paper, the choice seems straightforward. “Building” gives you control and flexibility; “buying” gives you speed and convenience. In reality, the trade-offs run much deeper, especially when you look through the lens of **Total Cost of Ownership (TCO)**.

Over the last few years, I’ve seen and have been part of teams starting with a DIY approach. State-of-the-art, terraform, containers, Airflow, dbt core, the works. It feels empowering: you control the stack, optimize for cost, and get to build something elegant and custom.  
But as months pass, the picture changes. What starts as an engineering playground quickly becomes a maintenance treadmill.

Let’s unpack why that happens and how TCO helps reveal the real dimensions of “make vs. buy.”

---

## 1. The Illusion of Control

In young or fast-growing companies, building in-house looks attractive.  
Your engineers are smart, cloud resources are cheap, and modern tools make ELT development easier than ever. Spinning up your own containerized, Terraform-managed stack seems like the “grown-up” thing to do.

The appeal is real:
- You get **full control** over the architecture.  
- You can **fine-tune costs** and skip expensive SaaS tiers.  
- You stay **independent from vendors** and keep your data in your own hands.

But control comes at a price and not always the one you expect.

---

## 2. TCO: Not on the Invoice

When people compare solutions, they usually look at the obvious:  
- Cloud compute  
- Storage  
- SaaS subscriptions  

That’s only part of the story. The **Total Cost of Ownership** adds layers most teams don’t quantify:

- **Engineering Time**: Hours spent writing Terraform modules, debugging Airflow DAGs, and patching dependencies.  
- **Context Switching**: Analysts and data engineers stuck between infra, ingestion, and transformation tasks.  
- **Operational Fatigue**: Handling downtime, schema drift, and pipeline failures.  
- **Talent Lifecycle**: Building infra roles that you might not need a year later.  

In other words: your cloud bill isn’t your TCO. Your *team calendar* is.

---

## 3. Slow Data Stacks

The biggest hidden cost in “make” decisions is **time-to-value**.

Standing up your own ELT platform sounds good, but getting from a prototype to a reliable, production-grade setup takes months. Every layer, orchestration, logging, secrets management, observability, CI/CD, needs attention. By the time everything runs smoothly, your team might already have shifted focus.

And here’s the painful part:  
Once the system is stable, the *infrastructure engineers you hired for setup are no longer critical*. You’ve built a platform that mostly runs itself but you still have the overhead of maintaining it, and often, a team whose core contribution was front-loaded.

That’s the part of TCO that’s rarely modeled: the cost of **building a team you don’t really need long-term**.

---

## 4. Renting Velocity

Managed solutions like **Astronomer** or **Dagster** might flip that equation. You’re not paying for software features, you are paying to *not think about infrastructure*. Setup takes days, not months. Pipelines run reliably out of the box. Your team stays focused on delivering value.

Of course, it comes with trade-offs:
- You’ll pay more per seat or per run.  
- You’ll have less control over the runtime.  
- You’ll live with vendor roadmaps and SLAs.

But here’s the thing: **for small and mid-sized teams, that’s a feature, not a bug**.  
When you’re still finding your analytical footing, outsourcing stability and observability can save you months of setup and years of maintenance.

---

## 5. TCO Is Multi-Dimensional

Thinking about TCO as just “cost” misses the point. It’s multi-dimensional, it’s about **focus**, **speed**, and **risk**.

| Dimension | DIY Bias | Managed Bias | Typical Tradeoff |
|------------|-----------|---------------|------------------|
| **Initial Cost** | Lower (infra only) | Higher (subscriptions) | DIY wins early |
| **Time-to-Value** | Slow | Immediate | Managed wins by months |
| **Maintenance** | Continuous | Offloaded | Managed wins long-term |
| **Flexibility** | Full control | Limited knobs | DIY wins if you truly need customization |
| **Team Focus** | Infra-heavy | Analytics-heavy | Managed lets you focus on insights |

For small teams especially, time-to-value and focus often outweigh control. You can always bring pieces back in-house once you outgrow the managed layers.

---

## 6. The “Lifecycle Trap”

There’s a lifecycle pattern that repeats across organizations:

1. **Exploration Phase:** DIY looks attractive - flexibility and cost savings.  
2. **Implementation Phase:** The team grows to build infra. Progress is slow but exciting.  
3. **Stabilization Phase:** Infrastructure is done, but now the team’s focus shifts. Engineers become platform maintainers instead of value creators.  
4. **Realization Phase:** You start evaluating managed solutions again to regain velocity.

Most companies could skip phases 1–3 entirely if they were honest about their priorities. Unless your data platform *is* your product, **you probably don’t need to own your stack end-to-end**.

---

## 7. Conclusion: Buy Back Your Focus

The build vs. buy debate isn’t really about cost. It’s about **what your team’s time is worth**.

Building your own ELT stack with Terraform, containers, and open-source tools can be an educational and empowering experience. But in most smaller setups, it’s a distraction. You spend six months building a platform so you can finally start delivering insights - only to discover that a managed platform could’ve had you there in six weeks.

Total Cost of Ownership isn’t just about money.  
It’s about *focus, time, and the kind of team you want to grow*.  
Buy if you want to move fast and learn about your business.  
Build if your data platform itself is part of your business.

But whatever you do...

**Make sure you’re measuring the cost of ownership, not just the cost of the invoice.**
