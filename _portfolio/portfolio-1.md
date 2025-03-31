---
title: "Impossible Okta Logins"
excerpt: "Custom-built User Behavior Analytics solution for Impossible Travel <br/><img src='/images/Impossible-Travel-Featured-Image.png'>"
collection: portfolio
---

Our "Impossible Travel" alert from Okta logins was noisy, with many false positives, and had been for years. Incident Response (IR) asked us to pursue resolution, and I took it on as a challenge. First, I used some whitelisting tricks to reduce noise, for instance against Amazon Virtual Desktop Infrastructure IPs. But after all whitelisting options had been pursued, the alert was still too noisy, so I took a more creative approach. 

I used Splunk Tables and Jobs to create a mechanism by which each Okta login event would be assigned a risk score, based on its deviance from historical data, on as many data factors as were available. Then, after working with Incident Response on an acceptable risk level, a risk threshold was set, below which alerts would not be surfaced. This reduced noise for the Incident Response team by a factor of 95% and resolved a long-lived pain point, while ensuring that abnornmal login events would still be seen and triaged by IR.
