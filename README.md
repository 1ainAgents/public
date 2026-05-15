# 1ain — Personal AI Agent System
**Visibility:** Public

## What is 1ain?
1ain (pronounced "main") is a personal master AI agent — the hub of a private,
self-hosted AI operating system. Built on Claude API, deployed on a personal VPS,
accessed via Telegram.

## Architecture
Hub-and-spoke: 1ain is the single interface to all AI capabilities.
Specialist agents route through 1ain — one interface, all capabilities.

```
Subject → Telegram → 1ain → [specialist agents]
                     ↑
              Soul template
              (persistent identity)
```

## What's Here
- `visuals/` — Architecture diagrams, roadmap, avatar, image generation prompts

## What's Not Here
Technical implementation, soul template, build documentation, and agent specifications
are private. This repository contains only visual and overview materials.

## Stack
Claude API · Python · Docker · Telegram · Self-hosted VPS · Git
