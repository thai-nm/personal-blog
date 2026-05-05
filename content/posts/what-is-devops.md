---
title: "What is DevOps?"
date: 2026-03-29
---

## Introduction

What exactly is DevOps?

It's a question that every engineer in this field has likely asked. After three years as a DevOps Engineer, experienced both outsourcing and global product company, I've developed a personal perspective on the definition of DevOps.

## Why DevOps?

In modern software development, the goal is to reduce risks and achieve faster feedback by deliver small but frequent updates. To achieve this, we need a way to bridge the gap between development and operations. That bridge is **DevOps**.

While many define DevOps as a "culture" or "philosophy", from my experience, it would be more practical to look at what a DevOps Engineer actually does.

## The Core Pillars

### 1. Automation (CI/CD)
Instead of manual deployments, we build automated pipelines. This ensures that code moves from `dev` to `production` consistently and without human error.

For example: Using tools like **GitHub Actions** or **Jenkins**, a developer can deploy a service with a single click, knowing the pipeline will handle the build and deployment in minutes.

### 2. Infrastructure management

We manage infrastructure, like virtual machines or databases, manually or by using automation tools such as Terraform.

The Terraform snippet below is an example of how we can define our infrastructure as code (IaC).

```terraform
resource "aws_instance" "web_server" {
    ami           = "ami-0c55b159cbfafe1f0"
    instance_type = "t2.micro"
    tags = { Name = "DevOps-VM" }
}
```

### 3. Monitoring

We ensure the system stays healthy. This involves activities such as:
- Develop and maintain internal metric dashboards, alerting systems
- Participate in on-call rotation
- Ensure the system scale properly during big events

For instance, by using tools like **Prometheus** and **Grafana**, we monitor resource usage and set up alerts to fix issues before they affect users.

### 4. Security

We're managing infrastructure, where applications run on. If we can't secure it properly, it would be a gold mine for hackers after they gain access to our infrastructure.

A simple example: If our database is "accidentally" exposed publicly, hacker can try to brute force to get admin access, encrypt the whole database, and ask us to pay using Bitcoin if we want our data back.

That's a part of our job.

## Collaboration

Unlike imagination of many people about a "server" guy, DevOps engineer communicates with many teams:
- With developers: We build CI/CD pipelines, help troubleshoot their apps on production
- With QA: We automate their testing suites using automation pipelines
- With IT/Security: We collaborate with them on access controls and cloud security

## Challenges & Opportunities

DevOps is a huge area, I believe I can't know everything about DevOps in this time on Earth:
- Continuous Learning: The tech stack is vast (Networking, Cloud, Linux, Security).
- High Pressure: You are often the first responder when systems go down.
- Communication: You must translate complex infrastructure needs into terms other teams understand.

But it does have very compelling rewards:
- Impact: You architect and build the foundation that allows the entire company to move faster.
- Salary: According to many sources, the salary for DevOps/Cloud Engineer is very attractive, especially in Vietnam and even in this AI era. You can search yourself online.

## Conclusion

DevOps is an amazing role, at least for me. If you are curious about computers, how things work under the hood, eager to learn more, you probably love DevOps, just like me. If you are someone who does not like to sit in front of the computer hours every day, or you don't like to learn so many many many different concepts with each of them can lead to several rabbit holes, maybe DevOps is not for you. In the end, everything is relative, it's just a job.

I hope you guys enjoy it!
Thank you.