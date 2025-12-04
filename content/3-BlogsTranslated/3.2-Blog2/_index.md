---
title: "Blog 2"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---
# AWS FOR SAP

## Introduction

Migrating SAP landscapes to AWS gives enterprises the opportunity to modernize their infrastructure and leverage the elasticity of the cloud. Businesses can scale compute, memory, and storage within minutes and automate provisioning to reduce operational errors.

However, applying auto scaling to SAP Application Servers introduces complexity. Traditionally, organizations over-provision resources to avoid system slowdowns during peak load periods—resulting in paying for maximum capacity even when it’s not needed.

Native AWS components such as Auto Scaling groups, Target Groups, and Launch Templates do not fully address SAP’s architectural requirements. To solve this challenge, AWS Professional Services developed the **SAP Auto Scaling solution**, enabling horizontal scaling of SAP Application Servers and reducing infrastructure costs by up to **50%**.

---

## Business Case for Auto Scaling

The SAP Auto Scaling solution is designed to address real operational challenges, such as:

- Ensuring SAP environments dynamically adapt to workload demand—scaling out during peak load and scaling in when demand drops.
- Allowing administrators to proactively activate or deactivate servers for maintenance or system upgrades.
- Reducing operational overhead by automating routine infrastructure tasks.

This solution provides the greatest value for customers who:

- Experience uneven workload cycles (e.g., lower usage during evenings or weekends).
- Are looking to reduce EC2 spend during off-peak hours.
- Operate production environments with **three or more** SAP Application Servers.
- Prefer flexible cost models without long-term commitments.

### Key Benefits

- Modernizes SAP environments by applying native cloud elasticity.
- Achieves significant EC2 cost savings—up to **50%** compared to running On-Demand instances continuously.
- Supports predictable scaling patterns aligned with business demand.

---

## How the Solution Works

SAP Auto Scaling automatically manages the active or inactive state of SAP Application Servers. It continuously monitors the usage of **Dialog Work Processes** on the ASCS (ABAP SAP Central Services) instance to determine when to scale.

### Core Functionality

- When load increases, the system starts a preconfigured EC2 instance and automatically launches its SAP services.
- Scale decisions (up or down) are based exclusively on Dialog Work Process utilization on the ASCS.
- Before a scale-down event, all active SAP GUI users receive an on-screen notification to save their work and reconnect.
- SAP Soft Shutdown ensures all batch jobs are completed before a server is turned off.
- Administrators can schedule start times for Application Servers.
- “No-scale windows” can be defined to block scaling during critical business hours.
- Critical servers can be marked as “always on.”
- Email notifications are sent for all scale events.

---

## Scale-Up Decision Tree

The system follows a structured 