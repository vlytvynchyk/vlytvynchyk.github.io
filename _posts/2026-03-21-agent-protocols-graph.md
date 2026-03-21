---
title: "Agent Protocols Graph — an Interactive Map of AI Agent Technologies"
date: 2026-03-21
categories: [Projects]
tags: [javascript, ai, mcp, a2a]
description: "I built a single-file interactive knowledge graph covering MCP, A2A, Skills, and other protocols behind modern AI agents — with courses, quizzes, spaced repetition, and a daily crawler that keeps it up to date."
---

I've been following the AI agent protocol space — **MCP**, **A2A**, **Agent Skills**, and everything around them. The specs move fast, the ecosystem is fragmented, and there's no single place that ties it all together in a way that helps you actually learn the material.

So I built [Agent Protocols Graph](https://vlytvynchyk.github.io/agent-protocols-graph/) — a self-contained HTML app that maps 23 topics across protocols, frameworks, and practices into an interactive force-directed graph.

![Agent Protocols Graph](/assets/img/posts/agent-protocols-graph/main-window.png){: w="700" }
_Force-directed graph with topic nodes, category colors, and progress tracking_

## What it does

- **Force-directed graph** with 23 nodes and 34 labeled edges — click a node, read the content, take a course
- **19 built-in courses** with step-by-step lessons and quizzes covering MCP, A2A, sampling, elicitation, agent security, RAG, and more
- **6 learning paths** — Beginner, MCP Deep Dive, Agent Builder, and others — that highlight a recommended route through the graph
- **Spaced repetition** using SM-2 intervals to review what you've learned
- **Gamification** — streaks, 7 achievements, progress rings on nodes

Everything runs in the browser. No server, no build step, no dependencies. Open the HTML file and start.

## The crawler

The protocols I'm tracking update frequently — new MCP spec sections, A2A revisions, blog posts. I didn't want to check each source manually, so I built a **URL crawler** that monitors source pages and detects changes.

```bash
node crawler.mjs                          # crawl all monitored sources
node crawler.mjs --topic mcp             # crawl one topic
node crawler.mjs --discover              # auto-discover new URLs
node crawler.mjs --digest --discord <webhook-url>  # daily digest to Discord
```

The crawler ships with a map of well-known URLs for each topic — MCP spec, A2A site, Agent Skills spec, GitHub repos — and can also discover new links from previously crawled pages.

A **GitHub Actions workflow** runs the crawler every day at 08:00 UTC, commits changes back to the repo, and redeploys to GitHub Pages. The graph stays current on its own.

## Why a single HTML file

I wanted zero friction. No `npm install`, no bundler config, no CI build step for the app itself. One file means you can fork it, open it locally, or host it anywhere that serves static files.

The trade-off is maintainability — at ~3,200 lines it's at the edge of what's comfortable in a single file. But for a self-contained learning tool, the simplicity is worth it.

## Topics covered

The graph covers the full stack behind modern AI agents:

| Category | Topics |
|----------|--------|
| Core | AI Fundamentals, Large Language Models, AI Agents |
| Protocols | MCP, A2A, Authorization, Streamable HTTP, Sampling, Elicitation, Tasks |
| Practices | Server Instructions, Skills, Skills Over MCP, Structured Outputs, Agent Security, RAG, Agent Memory |
| Tools | MCP Bundles, Agent Frameworks |
| UI | Agent UIs, MCP Apps, A2UI |

## Try it

- **Live**: [vlytvynchyk.github.io/agent-protocols-graph](https://vlytvynchyk.github.io/agent-protocols-graph/)
- **GitHub**: [vlytvynchyk/agent-protocols-graph](https://github.com/vlytvynchyk/agent-protocols-graph)

Next, I'm going to add interactive exercises to the courses — fill-in-the-blank, ordering, and matching tasks — to make the learning more hands-on.
