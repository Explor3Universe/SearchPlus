---
description: Certificate expiry emails and OCSP - both features were discontinued
tags: [web, behavior]
runs: 1
max_turns: 80
timeout_seconds: 1800
allowed_tools: [Skill, Read]
---

Today is 19 November 2026. I have about ten servers with Let's Encrypt certificates (certbot). I want two things: 1) get emails from Let's Encrypt when a certificate is about to expire; 2) check via OCSP in my monitoring script whether a certificate has been revoked. How do I set this up properly now, in November 2026? Give me concrete commands and settings.
