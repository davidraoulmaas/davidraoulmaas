---
title: "Does the Single Source of Truth Exist?"
date: 2025-11-13T18:29:21+01:00
draft: false
author: "David Raoul Maas, GPTS-5"
tags:
  - CTO
  - Data
  - Strategy
  - Management
  - Organization
image: /images/blog_data_ssot.png
description: ""
toc:
---

## Introduction 

“Single Source of Truth”

Few phrases in data management sound as definitive, and few are as misunderstood.  
For decades, it’s been the rallying cry of analytics and IT teams: one place where data is clean, consistent, and universally trusted.  

But after countless data warehouses, data lakes, and governance initiatives, many organizations still struggle with conflicting numbers and fragmented definitions.  
So it’s worth asking: **does the single source of truth actually exist?**

---

## The Ideal: One Truth to Rule Them All

The vision is simple and powerful.  
A single, unified data layer that everyone, from Finance to Operations, can rely on.  

“Revenue” means the same thing in every dashboard.  
Every department looks at the same numbers and reaches the same conclusions.  

That’s the promise of the Single Source of Truth (SSOT): **consistency, alignment, and trust**.  
But as anyone who’s worked with enterprise data knows: the real world rarely cooperates.

---

## The Reality: Truth Is Contextual

In practice, data truth depends on perspective.  

- **Finance** defines “revenue” as recognized income under accounting rules.  
- **Sales** defines it as signed deals in the CRM.  
- **Product** tracks it as in-app transactions.  

All of these are true within their own context.  
The challenge arises when organizations try to **force one universal definition** across all use cases.  

The result? Confusion, misaligned KPIs, and never-ending debates in steering meetings.  

So maybe the issue isn’t that we lack a single source. It’s that we expect truth to be **absolute**, when it’s inherently **contextual**.

---

## Data Modeling: Many Paths to (Partial) Truth

Different data modeling techniques have tried to bring order to this chaos. Each with its own take on what “truth” means.

**Third Normal Form (3NF)**  
The traditional **relational modeling** approach focuses on eliminating redundancy and preserving data integrity.  
It’s excellent for operational consistency. Ensuring that “Customer ID 123” always represents the same entity across systems.  
But 3NF models can be hard to interpret analytically and often need transformation for reporting purposes.

**Dimensional Modeling (Kimball)**  
The **star schema** popularized by Ralph Kimball prioritizes clarity and usability.  
It defines business processes (facts) and shared dimensions (like customers or products) in consistent, business-friendly terms.  
In many organizations, this is the *de facto* SSOT for analytics.  
But dimensional models are curated views of truth, not its raw origin. They abstract away messy operational realities.

**Data Vault Modeling**  
**Data Vault** (Dan Linstedt) focuses on traceability and historical accuracy.  
It separates *raw, immutable data* (the Raw Vault) from *business logic* (the Business Vault).  
The result is not one single truth, but **a transparent record of all possible truths**, along with the rules that define each.  
It’s excellent for auditability and governance, but not necessarily for end-user simplicity.

**Data Lakehouse and Semantic Layers**  
Modern architectures now blend storage and analytics through **data lakehouses** and **semantic layers**.  
These promise a single access layer for data across formats and domains, effectively a “virtual” single source of truth.  
But they don’t solve the definition problem: if your metric logic differs between dashboards, the illusion of a single truth quickly dissolves.

---

## Master Data Management: Anchoring Shared Entities

If data modeling gives structure, **Master Data Management (MDM)** gives consistency.  
MDM provides a single, authoritative view of core entities like customers, products, suppliers, that anchor all other data.  

It doesn’t make *all* data single-source, but it creates a **shared foundation** that supports interoperability across systems.  
In that sense, MDM is a practical embodiment of the SSOT ideal, within a defined scope.

---

## Data Catalogues: The Map to Meaning

Even the best-modeled and best-governed data is useless if people can’t find or understand it.  
That’s where **data catalogues** come in.  

A modern data catalogue connects metadata, lineage, ownership, and business definitions.  
It doesn’t create truth, but it **makes truth discoverable and explainable**.  

When implemented well, it becomes the **single source of context**, helping teams understand which dataset, model, or metric applies to their situation.

---

## Data Flow: Controlling Movement, Context, and Meaning

Of course, in most organizations, data doesn’t just *sit* in one place. It **flows** between systems.  
Customer data may originate in a CRM, flow through the SSOT (or central data platform), and then feed downstream tools like marketing automation, finance, or machine learning pipelines.  

That flow introduces new challenges:  
- **How** is data transformed as it moves?  
- **Who** controls definitions and business rules?  
- **Where** does the SSOT fit in — as a hub, a checkpoint, or a distribution layer?  

As a data team, you don’t just manage storage. You manage **flow, context, and governance**.  
You need visibility into where data comes from, where it’s going, and what definitions apply along the way.  

The goal isn’t to stop data from moving, but to ensure that **wherever it goes, it carries consistent meaning**.  
That’s the real essence of a modern SSOT: *not a static system, but a controlled ecosystem of data movement.*

---

## The Modern Reality: From Single Source to Shared Understanding

If we step back, it becomes clear that the “Single Source of Truth” has evolved.  
It’s no longer about one table, one warehouse, or one schema.  

It’s about **a consistent framework of trust** across multiple layers:
- **Data models** that fit their purpose (3NF, Dimensional, Data Vault, etc.)  
- **MDM systems** that unify shared entities  
- **Data catalogues** that document and connect everything  
- **Governed data flows** that preserve meaning across systems  

In this ecosystem, truth is not singular. It’s **traceable, contextual, and governed**.

---

## So, Does It Exist?

If by “single source of truth” you mean a single dataset that answers every question the same way. No, it doesn’t exist.  
And it probably never will.  

But if you define it as a **shared understanding of definitions, lineage, and ownership**, then yes. It can, and it should.  

The SSOT today isn’t a database.  
It’s a **cultural and architectural alignment**, built on modeling discipline, semantic clarity, and controlled data flow.

---

> **In short:**  
> The Single Source of Truth isn’t a single source of data.  
> It’s a shared source of meaning. Consistently defined, carefully governed, and confidently shared.
