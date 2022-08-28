
# Lean Secure Software Delivery 
## How to make my organization dev-sec-ops ready?
One of the main challenges that organizations are facing is how to protect and secure their business in the current day of ever evolving cyber treats. This post will try to guide navigate the wide security domain by exploring available options and how they can be utilized to make security build into your applications. 
> Lessons and best practices from years of work across  projects, teams and cultures pertaining to Lean secure software delivery.
#ShiftLeft #SecureSDLC #DevSecOps
 
### Before State
Security is a after thought and a necessary evil that software delivery teams have to deal with to release software/products.
- A manual process with help of tools to review applications and identify security issues.
- Creating security bugs or tasks for high risk issues that need to be fixed before release.
- Teams struggle to fix the issues leading to the expensive (time and money) sdlc cycle with most of the failing to release in time or releasing with accepted risk.
- Most of the fixes end up creating substantial technical debt and effects code quality.
- Most of the medium and low vulnerabilities end up in backlog and typically never looked at.
- With growing pressure from business to release will end up creating risk tickets being accepted and vulnerable applications running in production.

###  Current State 

Security is integrated into the development life cycle from project initialization so security aspects are planned, implemented, identified and fixed early.  Essentially its ingrained into the day to day SDLC of teams.  This helps to made teams deliver secure software faster.


### How can you get there...
#### Prerequisites for DevSecOps
The shift to a continuous development, build, deployment and monitoring framework with appropriate security controls and checks embedded into appropriate phase. Building the new workflow with coordination from your development teams,  security teams and operation and monitoring teams.

#### Implementation:

 - DevSecOps Platform components
	 - Source Code repositories like github, bitbucket to store and manage all source code.
	 - Build Tools like maven, gradle, SBT to compile and build deployable artifacts.
	 - CI/CD tools like Jenkins, AWS codebuild and codedeploy to build, test and create pipelines with deployment steps
	 - Artifactory like docker hub, jfrog to store your build artifacts.
	 - Deployment tools to deploy and run your build artifacts.
	 - Monitoring and reporting tools to review various checks at each stage and report.



Review your current software delivery workflow and identify the best places to embed appropriate security tools and processes.
 
 The best place to fix a bug is on a developers  machine before he commits this code. So this is good option and we should try to best utilize via various security [IDE plugins](https://ayalamanchili.github.io/secure-code-ide-plugins.html).
 
At core most delivery pipelines will have some process to build code deploy code to various environments where apps get vetted before moved to higher environments. Identify the lowest environment where security tools can be embedded and how the various issues reported by tools can be  triaged, vetted and delivered to the app teams, in most cases it could a development environment where tools can be embedded and setup to create bug tickets for applications. 
 > its important to tune the tools to minimize false positives to minimize noise to app teams  or you will need to add a additional triage layer to validate before sending to app teams
### Below are various tool categories that can be utilized.
 - [SAST](https://ayalamanchili.github.io/sast.html)
-  [IAST](https://ayalamanchili.github.io/iast.html)
-  [OSS](https://ayalamanchili.github.io/oss.html)
- [Compliance](https://ayalamanchili.github.io/compliance-tools.html)
- [Treat Modeling](https://ayalamanchili.github.io/treat-moedling.html)
- [Web Scanners](https://ayalamanchili.github.io/web-scanners.html)
### Sample SDLC workflow with potential best phases to embed your security tools.


![enter image description here](https://docs.google.com/drawings/d/e/2PACX-1vSZPaBFhSQrnUSqV8uiEOB2HVmzsO1p9Gc-7DFoNNGgmfcxA1JxReHFIlwd7dkhZi2bJ-iRsD3P9iJ0/pub?w=960&h=720)

#### Evaluate and identify the best tools for your stack and delivery stream. 
Depending on your technology stack, skills, infrastructure setup identify the best tools that fit your deployment landscape.

#### Build automation to integrate the tools to your delivery lifestyle on the most left as possible
Most of the popular tools have a lot of integration points with CI/CD tools. its important to invest in building automation to make it simple for new/existing application to get on-boarded.

#### Onboard your applications
Onboard your application with this tools so the tools are scanning and running with your applications. This will ensure your security tasks and issues are identified and reported to the necessary members and team for action.
