---
title: "The Evolution of Data Architecture"
date: 2025-11-05T13:29:21+01:00
draft: false
author: "David Raoul Maas, GPTS-5"
tags:
  - CTO
  - Data
  - Strategy
  - Management
  - Organization
image: /images/blog_data_evolution.png
description: "This post looks at the evolution of data architecture archetypes."
toc:
---

## Introduction

If you’ve been around data long enough, you’ve probably seen this movie before.  
First, we fell in love with *no-/low-code ETL tools* like SSIS, Matillion or Alteryx. Drag-and-drop nodes, colorful workflows, and a promise that “anyone can build data pipelines.”  
Then came the backlash: engineers wanted code, reproducibility, and control. Suddenly, everything had to be *in Terraform, Dockerized, and YAML-defined*.  

And now?  
We’re swinging back again, toward SaaS-first, declarative, and low-code data platforms.  
Only this time, it’s not because we want simplicity. It’s because **complexity finally became too expensive**.

Let’s walk through how this evolution happened — and what it tells us about where data architecture is heading next.

---

## 1. The First Wave

Back in the 2010s, the main challenge in data engineering was **getting data moved at all**.  
Cloud data warehouses were emerging, but teams were small, and few people could code scalable data pipelines from scratch.  

Tools like **SSIS, Pentaho, Matillion, or Talend** solved this.  
They offered:
- Visual workflows and reusable components  
- Quick setup for business logic  
- Rapid onboarding for analysts and IT staff  

They made ETL accessible. But also **opaque**.  
You could get something working fast, but six months later, no one knew what that green box actually did. Versioning, CI/CD, and testing were afterthoughts.  

These tools scaled teams. Until they didn’t.

---

## 2. The IaC Era

Around the mid-2010s to early 2020s, data teams began to mature technically.  
They wanted control, transparency, and the ability to *treat data like software*.  

Instead of dragging nodes, we:
- **Wrote transformations in SQL or Python**
- **Managed orchestration in Airflow**
- **Deployed infrastructure through Cloudformation, DevOps, Terraform**
- **Dockerized everything**, from extractors to transformers.
- Stitched it all together with open-source tools like **dbt, Meltano, or Prefect**

This was a huge step forward. Technically elegant, highly flexible, and, most importantly, *ours*.  
We were no longer locked into proprietary ETL GUIs.  

But it came at a price.  
Teams built enormous complexity into their pipelines, often without realizing they were reinventing vendor platforms.  
Data engineering turned into a **DevOps discipline**, not a value-creation one.

And for smaller orgs, it meant hiring engineers to maintain infrastructure that added little business differentiation.

---

## 3. The Next Wave

Now we’re seeing the next shift: **Data as a Service**.  

Modern platforms like **dbt Cloud, Airbyte Cloud, Fivetran, Astronomer, Snowflake Native Apps**, and even **data-as-a-platform** offerings are moving the stack back up the abstraction ladder.  

They’re not “low-code” in the old sense. They’re **high-leverage**.  
You still write SQL or Python, but you don’t need to maintain Dockerfiles, YAMLs, or Terraform modules just to run them.  

This new low-code era isn’t about hiding complexity; it’s about **outsourcing undifferentiated complexity**:
- Managed orchestration instead of Airflow clusters  
- SaaS-native connectors instead of homegrown ELT scripts  
- Declarative configuration (“what”) instead of procedural operations (“how”)

You focus on data models, quality, and insights. Not on keeping containers alive.

---

## 4. Why the Pendulum Swings Back

Every technical discipline moves in cycles.  
Abstraction goes up when teams crave productivity, and down when they crave control.  

Data engineering is no different.

| Era | Motto | Core Trade-off |
|------|-------|----------------|
| **Low-Code ETL (2010s)** | “Make it easy for anyone.” | Fast to start, slow to maintain |
| **DIY Infrastructure (2020s)** | “We need control.” | Powerful, but expensive in people |
| **SaaS / Data-as-a-Service (Now)** | “Focus on what matters.” | Outsourced ops, vendor dependency |

We’re learning that **control is not always value**.  
Just because you *can* Dockerize and Terraform your entire ELT stack doesn’t mean you *should*.  

Unless you’re a platform company yourself, the ROI on fully custom infrastructure is usually negative after year one.

---

## 5. The Human Side of the Shift

Each architectural era also creates a different kind of data team.

- **Low-code ETL** → Business-heavy, tool-driven analysts  
- **DIY Era** → Infra-heavy, code-driven engineers  
- **Modern SaaS / Low-Ops** → Product-oriented analytics engineers  

That last one is important.  
The future of data isn’t about full-stack data engineers who manage Kubernetes clusters; it’s about **analytics engineers who ship value fast** on managed platforms.

That shift is as much cultural as it is technical.

---

## 6. Where We’re Heading

We’re entering a world where:
- Pipelines are declarative, not imperative  
- Infrastructure is rented, not built  
- Data products are versioned, tested, and observable out of the box  

The most successful data teams won’t be the ones with the most YAMLs, but the ones who understand **which parts of the stack to own** and which parts to delegate.

And ironically, after a decade of “everything-as-code,” we’re rediscovering that sometimes, the best code is **no code at all**.

---

## Conclusion

Data architecture has gone full circle:  
From drag-and-drop nodes → to code and containers → back to managed, declarative systems.

Each step solved a real problem and overcorrected in the process.  
What we’re seeing now is a more balanced era, where *low-code* doesn’t mean *low-control*, and *SaaS* doesn’t mean *shallow*.  

The lesson?  
Don’t fall in love with any particular stage of the pendulum.  
Focus on what your organization actually needs:  
**Speed, clarity, and sustainable ownership**. no matter how much code it takes.

