---
title: "AWS Compliance Audit via Gatekeeper"
excerpt: "Built innovative auditing solution to bypass sensitive security system<br/><img src='/images/nasa-gate.jpg'>"
collection: portfolio
---

Gatekeeper is a custom Okta tool that manages employee access to their AWS environments. We were asked to perform thorough evidence collection for an IGA audit across multiple platforms, and I took on the AWS portion, which was the hardest due to Gatekeeper. I used Python scripts to reproducibly, and with a high degree of assurance, pull hundreds of Users, with their Groups, Permissions, and related data from our AWS environment. 

The task was made particularly difficult due to the behavior of Gatekeeper, which would ban you if you used a library such as multiprocessing or threading, or "rocked the boat" in any way. Thus, a MongoDB database was used so that the application could be run idempotently, collecting only new data, until all the data was collected for the report.

The audit went smoothly, and the scripts are stored safely in a GitHub repo for the next time this task comes up.
