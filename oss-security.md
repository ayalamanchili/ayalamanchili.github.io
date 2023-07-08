## SCA
SCA stands for Software Composition Analysis. 
## Why SCA scans are needed ?
- More than 90% of all modern web applications use some open source dependencies.
- The average software uses around 148 open source components
- Growing vulnarabilities with open source librabies and raise in with supply chain attacks.

SCA tools/Scans help you detect and manage the security vulnarabilities in all open source components in your Orgs codebase.They also will help identify licensing information that requires attribution or policy compliance.

## SCA vs SAST
![sca-sast-overview.png]({{site.baseurl}}/static/sca-sast-overview.png)

## How to identify and remediate OSS vulnarabilities.
- Run SCA/OSS scan along with SAST scans early on in the SSDLC.
- This helps to identify addition of vulnarabilaties early on and block deployment of code to higher environments.

## What are the various options to run SCA/OSS scans.
 - Open Source
   - Dependency checker
   - Github
   - Gitlab
    
 - Commercial
   - Blackduck
   - Contrast
   - Snyk
   - Cycode




