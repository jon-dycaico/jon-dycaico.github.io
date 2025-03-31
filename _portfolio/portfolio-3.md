---
title: "Houston Structural Fix with Redis"
excerpt: "Remediated deep, long-term problems in our SOAR by designing and implementing a Redis-based solution <br/><img src='/images/redis.jpg'>"
collection: portfolio
---

This project highlighted my ability to struggle with an ambiguous problem, research to find solutions, and implement the chosen solution on a mission-critical asset - "Houston". Houston, our custom Rails SOAR had a problem: continually, but occasionally, we would see `Deadlock` errors and the job would fail, and in some cases the retries would fail, and the job would be lost. This is serious in a Security Monitoring environment, where that job may have been a criticial piece of information. So I was tasked with fixing it. 

I crawled the forums and GitHub discussion pages for related repos, dug into the Sidekiq job system, and found our solution - it was a simple race condition. Multiple job runs were occuring against the same SQL row, causing the deadlock. My solution was to implement a Redis store for our "high-velocity" data, which required reworking a lot of our Agent types. It also required careful integration with other components in the SOAR system. Once implemented in our dev instance, I tested the different agent classes, monitored the state of the Redis store, and confirmed that the solution would take. Moving to Production required additional break-fixes, but finally we had a SOAR we could trust. It also improved throughput significantly
