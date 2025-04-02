---
title: "SOAR Job-System Rewrite"
excerpt: "Remediated deep, long-term SOAR issues by designing and implementing a Redis-based solution <br/><img src='/images/redis.jpg'>"
collection: portfolio
---

*DocuSign*

This project highlighted my ability to struggle with an ambiguous problem, research to find solutions, and implement the chosen solution on a mission-critical asset: **Houston**. Houston, our custom Rails SOAR, had a problem: continually, but occasionally, we would see `Deadlock` errors and the job would fail, and in some cases the retries would fail, and the job would be lost. This is a serious issue in a Security Monitoring environment, where any job may provide the key information needed to resolve or properly alert on a security incident. So I took it on. 

I crawled the forums and GitHub discussion pages for related repos, dug into the `Sidekiq` job system, and found our solution: a race condition. Multiple jobs were running against the same SQL row simultaneously, causing the deadlock. My solution was to implement a `Redis` store for our "high-velocity" data, which required reworking many of our Agent types, and careful integration with the backend components of the SOAR system. 

Once implemented in our *DEV* instance, I tested the different agent classes, monitored the state of the Redis store, and confirmed that the solution would take. Moving to Production required additional break-fixes, but finally we had a SOAR we could trust. As a bonus, it significantly improved system throughput, which helped keep us going until Houston's eventual replacement.