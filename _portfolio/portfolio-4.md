---
title: "Gmail Migration"
excerpt: "Rebuilt all our Email and Directory automation against Google Workspace APIs <br/><img src='/images/google-workspace.png'>"
collection: portfolio
---

Up until this point, we had been using [Huginn's](https://github.com/huginn/huginn) native Email Agent and Email Digest Agent for all email tasks, and the Post Agent for employee info lookups, all running against Microsoft 365 APIs. Once the company decided to go with Google Workspace, it was up to me to migrate all of this logic, not only into new agents, but to design and build the new Agent classes myself. 

This required digging into the Google Workspace APIs, setting up OIDC authentication, writing the Agent code in Rails, validating the new Agent types in our development environment, then migrating 50+ existing Agents across our Playbook infrastructure to the new models, and finally, careful validation of the resulting flows. Ongoing tuning work was required to keep our Playbooks healthy and the mail-flow reliable, but at the end of it all, we had nice, reliable Agents for our Email and Employee Lookup use cases that had the appropriate permissions in Google Workspace and were more reliable and feature-filled than the previous state. 
