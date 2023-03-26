

# SAST Orchestration
Process of analyzing static source code to identify and report security vulnerabilities. 
TODO high level pic 
 
All new and existing projects will be on boarded to a security automation platform that will listen to code changes and runtime testing on developer machine and/or lower environments. we add listeners/webhooks that will listen to the changes in code/runtime and perform a variety of security checks in background using various [security testing automation tools and frameworks](https://ayalamanchili.github.io/security-testing-automation-tools.html). If a issue is found the its first sent to first response team to triage who will validate the issue which if is a valid finding will create a Bug for project team. This process typically happens with in ~4 hours from the moment the vulnerable code is checked in. 
 As teams get notified with tickets with the needed details pertaining they can fix it and the Security orchestration will listen and run validated checks and if passed will close the issue and notify team.
 
## How to Integrate 

**Approach #1:** Add build step to trigger SAST code scan as part of your CI/CD pipeline.  So as software gets build that triggers the pipeline will runs scans.
**Pros:**
 - makes security scans part of your existing software delivery pipeline
 - can easily configure  to fail insecure builds to be promoted to higher environments

 **Cons:**
 - improper tuning of scan setting will result in too many false positives which results in wasted cycles.
 
**Approach #2:**  Build orchestration software to listen to code changes across projects and trigger code scans for projects independent of application CI/CD pipelines.
**Pros:**
 - independent background process that runs behind the delivery pipeline and only notifies when there is a validated issue

**Cons:**
 - no active involvement of development teams except to fix issues

Approach #1 fares well with org/team culture which is more open and ready to embrace security into their life cycle.
Approach #2 fares well with org/team culture which sees security as a separate aspect. 

## SAST scan tools

There are a variety of [SAST Tools](https://owasp.org/www-community/Source_Code_Analysis_Tools) available. please reivew and pick the one best for your case.


## What happens after scans

 - As scans run and report issues its important to **tune** and/or **validate** (remove false positives) this is a essential step to remove the noise and only channel the confirmed ones to the attention of development teams.
 
 

