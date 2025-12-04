---
title: "Event 2"
date: 2025-11-29
weight: 2
chapter: false
pre: " <b> 4.3. </b> "
---

# Summary Report: “AWS Well-Architected — Security Pillar Workshop”

### Event Objectives

- Provide a structured understanding of the **Security Pillar** within the AWS Well-Architected Framework  
- Highlight essential security principles such as **least privilege**, **zero trust**, and **defense in depth**  
- Explain AWS’s **Shared Responsibility Model** and its practical implications  
- Explore common cloud security threats in the Vietnam context  

### Key Highlights

#### Opening & Security Foundations

- Clarified the strategic role of the Security Pillar in modern cloud architecture  
- Reviewed core security concepts: minimal access rights, distrust-by-default, and layered protection  
- Explained how responsibilities are divided between AWS and customers  
- Discussed major cloud security risks frequently observed in Vietnam-based workloads  

#### Pillar 1 — Identity & Access Management

##### Modern IAM Architecture

- Emphasized designing IAM systems around **users, roles, and policies**, eliminating long-term credentials  
- Introduced **IAM Identity Center** for centralized permission management and SSO  
- Demonstrated the use of **SCPs** and **permission boundaries** in multi-account setups  
- Reinforced security through **MFA**, periodic credential rotation, and Access Analyzer evaluations  
- Featured a mini demo on policy validation and access simulation  

#### Pillar 2 — Detection

##### Detection & Continuous Monitoring

- Showcased **CloudTrail**, **GuardDuty**, and **Security Hub** for continuous detection coverage  
- Highlighted multi-layer logging: VPC Flow Logs, ALB access logs, and S3 audit logs  
- Demonstrated configuring alerts and automation using **EventBridge**  
- Introduced the concept of **Detection-as-Code** for standardized monitoring rules  

#### Pillar 3 — Infrastructure Protection

##### Network & Workload Security

- Outlined network segmentation strategies and proper public/private resource placement  
- Compared effective use cases for **Security Groups** versus **NACLs**  
- Explained perimeter defense using AWS **WAF**, **Shield**, and **Network Firewall**  
- Reviewed fundamental security practices for workloads running on EC2 and container services (ECS/EKS)  

#### Pillar 4 — Data Protection

##### Encryption, Keys & Secrets

- Introduced AWS **KMS** for key lifecycle management: policies, grants, and rotation  
- Covered encryption best practices across S3, EBS, RDS, and DynamoDB  
- Demonstrated secure secret storage with **Secrets Manager** and **Parameter Store**, including rotation patterns  
- Explained data classification and appropriate access controls  

#### Pillar 5 — Incident Response

##### IR Playbook & Automation

- Walked through AWS’s incident response lifecycle and best practices  
- Provided sample playbooks for:  
  - Stolen or exposed IAM credentials  
  - Publicly accessible S3 buckets  
  - Malware detection on EC2 instances  
- Demonstrated snapshotting, isolating compromised resources, and evidence collection  
- Showcased automated remediation using Lambda and Step Functions  

### Key Takeaways

- AWS security relies on layered controls across identity, detection, infrastructure, data, and incident response  
- Multi-account governance with managed access improves operational and security posture  
- Logging, detection, and automation are essential for real-time visibility  
- Proper encryption and secrets management are critical for maintaining data integrity  
- Automated incident response reduces resolution time and limits impact  

### Applying to Work

- Strengthen IAM controls by moving fully to role-based access and short-lived credentials  
- Implement centralized monitoring across accounts with GuardDuty, CloudTrail, and Security Hub  
- Enforce network segmentation and apply the principle of least privilege at the network layer  
- Adopt KMS and Secrets Manager for secure encryption and credential management  
- Develop IR playbooks and automate responses for common security scenarios  

### Event Experience

Engaging in the Security Pillar workshop at AWS Vietnam provided a comprehensive view of best practices for designing secure, scalable cloud workloads.

#### Learning from AWS Specialists

- Gained clear insights into how AWS structures its security services and best practices  
- Real-world security scenarios illustrated how threats can be mitigated with AWS-native tools  

#### Hands-on Understanding

- Demonstrations made complex concepts like policy simulation, log analysis, and automated responses easy to grasp  
- The IR workflow examples highlighted practical steps to contain incidents efficiently  

#### Practical Insights

- Emphasis on multi-account security and continuous monitoring provided strong guidance for enterprise environments  
- Understanding detection patterns and guardrails clarified how to maintain compliance at scale  

#### Networking Opportunities

- Connected with cloud engineers and AWS experts to exchange experiences in securing cloud infrastructure  
- Discussions revealed common pitfalls and successful security approaches used across Vietnam  

#### Lessons Learned

- Strong IAM controls are the foundation of cloud security  
- Automation significantly reduces risk and operational overhead  
- Incident response readiness is essential for minimizing damage and downtime  


> Overall, the workshop delivered deep insights and actionable guidance to strengthen cloud security practices, reinforcing the importance of a well-architected security-first mindset.
