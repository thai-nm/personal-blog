---
title: "Setting up Claude app with private remote MCP servers"
date: 2026-08-09
categories: ["devops"]
tags: ["ai", "devops"]
dek: "A small effort of myself to learn about MCP servers and how to deploy them securely."
---

## Introduction

What is your favourite MCP server?

For me it's Excalidraw MCP server. Excalidraw is a great open-source tool to sketch all types of diagram. Now with the power of generative AI, we can even create diagrams much easier and faster. These diagrams can then be used for self-learning, technical documentation and presentation.

How are we connecting to an MCP server?

Normally if the external tool or datasources provide a remote MCP server, we can easily configure our coding agents such as Claude Code or Codex to connect to the remote MCP server. However, many other tools only provide the MCP server source code including some instructions to run it locally.

There are many problems with local MCP servers and here are some of them:
- For normal users:
  - We need to run the MCP server locally: More things to install, more dependencies to manage, different servers require different setup, etc.
- For enterprise:
  - Waste of resource and lack of standardized setup: Everyone spins up their own MCP servers with different configuration
  - Security risk: Untrusted MCP servers downloaded from internet can be misconfigured or contain malicious configuration and pose a critical threat to user and organization data.

As a DevOps or Platform engineer, we are usually tasked with standardizing the deployment process and consolidating scattered setups. In my homelab environment, I have several tools running and each of them provides their own MCP server. I also have 3 devices I want to connect to those MCP servers, and that would be a nightmare to set them up on each device. 

So I created one problem for myself: Configure once, run everywhere.

## Solution

I have a Kubernetes cluster running in my homelab to mimic enterprise environment.

We can deploy MCP servers on a VM like we usually do with normal HTTP servers. But since most of the workload nowadays are containers, my homelab Kubernetes cluster is an ideal candidate for the deployment.

Here is the simplified version of my current setup:

![Simplified architecture diagram](../../images/setting-up-claude-app-with-private-remote-mcp-server/simplified-architecture.png)


### High-level Implementation

This shows high-level implementation steps.

## Next steps

This shows limitations and improvement opportunities.
