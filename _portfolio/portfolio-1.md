---
title: "SOAR Migration Leadership"
excerpt: "Lead a Large Migration of all Security Automation logic from custom SOAR to Tines<br/><img src='/images/migration.jpg'>"
collection: portfolio
---

*DocuSign*

Once the risk and burden associated with maintaining our in-house SOAR, Houston, became too much for management to bear, and I was asked to find an alternative. First, I got to work evaluating more than 10 candidate SOAR platforms to see if they would fit our needs. When the selection process was complete, I catalogued all our SOAR Playbooks, all the resources they interacted with, and all affected teams. I then worked cross-functionally and independently to migrate our Playbook logic (code) into the new Platform. We went through a thorough Security Architecture Review and Threat Modeling process, for both the new platform and its extensions I built in AWS: [🦊](https://gitlab.com/soar_jd/aws-lambdas-for-tines)

I helped set up the new SOAR on an Azure Ubuntu server, using Linux system adminstration skills, Docker, and learning libvirt. The full system was end-to-end tested methodically and once my validation checklist was passing, we cut over to the new platform. This process resulted in a stable, rock-solid SOAR system that no longer required Ruby on Rails expertise to maintain, a skillset that is out-of-scope for most Security Engineering teams. It also opened the door for all of Tines' new features to be utilized by ourselves and our partner teams, in the long-run, increasing development speed and playbook reliability.


