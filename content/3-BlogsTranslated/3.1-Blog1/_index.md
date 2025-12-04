---
title: "Blog 1"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

# OpenAI Open-Weight Models Now Available on AWS

OpenAI’s open-weight models are now available on **AWS**, giving organizations and developers the ability to integrate advanced AI with greater flexibility, scalability, and control. These models are designed for **text generation, reasoning, programming, and scientific workloads**, with support for context lengths up to **128K tokens** and adjustable reasoning levels.

This blog post outlines the availability of OpenAI’s new models, the architectural choices behind their AWS integration, and how developers can get started using **Amazon Bedrock** and **Amazon SageMaker JumpStart**.

---

## Architecture Guidance

The new models — **gpt-oss-120b** and **gpt-oss-20b** — are available through both **Amazon Bedrock** and **Amazon SageMaker JumpStart**:  
- **Amazon Bedrock**: Provides serverless, API-driven access to models via `InvokeModel` or `Converse`.  
- **SageMaker JumpStart**: Enables fine-tuning, scalable deployment, and production integration using either the console or the Python SDK.  

**Solution architecture highlights include:**  
- Direct model access via Bedrock endpoints  
- Managed deployment options through SageMaker  
- Support for multi-service workflows and event-driven architectures  

---

While the term *open-weight models* is broad, some key characteristics include:  
- High flexibility with **custom deployment options**  
- **Transparency** through reasoning traces for interpretability  
- Designed for embedding into **event-driven and agentic workflows**  
- Compatibility with **OpenAI SDKs** and AWS-native services  

When evaluating deployment options, consider:  
- **Intrinsic factors**: context size, performance, reasoning quality  
- **Extrinsic factors**: scalability, integration requirements, reusability  
- **Human factors**: developer productivity, operational ownership  

---

## Technology Choices and Communication Scope

| Integration Scope             | AWS Services / Patterns to Consider                          |
| ----------------------------- | ------------------------------------------------------------ |
| Model access & testing        | Amazon Bedrock (chat playground, APIs)                      |
| Fine-tuning & deployment      | Amazon SageMaker JumpStart                                   |
| Event-driven workflows        | Amazon EventBridge, AWS Lambda, Bedrock AgentCore            |
| Tool-augmented AI agents      | Strands Agents with Bedrock-integrated models                |

---

## Hub-and-Spoke Analogy for Model Integration

Similar to a **pub/sub hub** used in microservices, AWS enables a hub-and-spoke approach for AI integration:  
- Models are accessed via **Bedrock endpoints**  
- Interactions are standardized through **OpenAI-compatible APIs**  
- Developers can switch between different foundation models without rewriting application logic  

**Trade-off:** careful **coordination and monitoring** are required to manage multiple models and reasoning levels effectively.  

---

## Core Model Access

The foundation for using OpenAI models on AWS includes:  
- **Amazon Bedrock** for serverless inference  
- **Amazon SageMaker JumpStart** for managed deployment and fine-tuning  
- **OpenAI SDK compatibility** for seamless integration  
- **Reasoning trace support** for improved transparency  

> These models are production-ready and optimized for integration with existing AWS workloads.  

---

## Developer Entry Point

- Access models through the **Amazon Bedrock console**: request model access and start testing in the chat playground  
- Authenticate via **AWS IAM policies**  
- Use the **OpenAI SDK** by pointing `OPENAI_BASE_URL` to the Bedrock runtime endpoint  

**Example Python code:**

```python
from openai import OpenAI

client = OpenAI()

response = client.chat.completions.create(
  messages=[{"role": "user", "content": "Tell me the square root of 42 ^ 3"}],
  model="openai.gpt-oss-120b-1:0",
  stream=True
)

for item in response:
    print(item)
