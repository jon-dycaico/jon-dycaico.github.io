---
title: "Impossible Okta UBA"
excerpt: "Custom-built User Behavior Analytics (UBA) solution for Impossible Travel alerts<br/><img src='/images/Impossible-Travel-Featured-Image.png'>"
collection: portfolio
---

*DocuSign*

Our "Impossible Travel" alert from Okta logins was noisy, with many false positives, and had been for years. Incident Response (IR) asked us to pursue resolution, and I took it on as a challenge. First, I used some whitelisting tricks to reduce noise, for instance against Amazon Virtual Desktop Infrastructure IPs. But after all whitelisting options had been pursued, the alert was still too noisy, so I took a more creative approach, and used the tools at my disposal to create a custom User Behavior Analytics pipeline.

I used Splunk Tables and Jobs to create a mechanism by which each Okta login event would be assigned a risk score, based on its deviance from historical data per-user, on as many data factors as were available. After some back and forth with the Incident Response team, the risk threshold was set, below which alerts would be suppressed. This reduced noise for the Incident Response team by a factor of 95% and resolved a long-lived pain point, while ensuring that abnornmal login events would still be seen and triaged by Incident Response.
