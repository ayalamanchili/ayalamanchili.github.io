---


---

<h1 id="lean-secure-software-delivery">Lean Secure Software Delivery</h1>
<h2 id="how-to-make-my-organization-dev-sec-ops-ready">How to make my organization dev-sec-ops ready?</h2>
<p>Lessons and best practices from years of work across  projects, teams and cultures pertaining to Lean secure software delivery<br>
#ShiftLeft #SecureSDLC #DevSecOps</p>
<h3 id="before-state">Before State</h3>
<p>Security is a after thought and necessary evil that software delivery teams have to deal with to release software/products.</p>
<ul>
<li>A manual process to review (via SAST tools) the software code identifying the vulnerabilities in code that was build and tested sometime back.</li>
<li>Creating security bugs or tasks for high risk issues that need to be fixed before release.</li>
<li>Teams struggle to fix the issues leading to the expensive (time and money) sdlc cycle with most of the failing to release in time or releasing with accepted risk.</li>
<li>Most of the fixes end up creating substantial technical debt and effects code quality.</li>
<li>Most of the medium and low vulnerabilities end up in backlog and typically never looked at.</li>
<li>With growing pressure from business to release will end up creating risk tickets being accepted.</li>
</ul>
<h3 id="current-state">Current State</h3>
<p>Security is integrated into the development life cycle from project initialization so security aspects are planned,implemented, identified and fixed early.  Essentially its ingrained into the day to day SDLC of teams.  This helps to made teams deliver secure software faster.</p>
<h3 id="how-can-you-get-there...">How can you get there…</h3>
<h4 id="review-your-software-delivery-workflow-and-identify-the-best-place-to-embed-security-tasks-and-issues.">Review your software delivery workflow and identify the best place to embed security tasks and issues.</h4>
<p>The best place to fix a bug is on a developers  machine before he commits this code. So this is good option and we should try to best utilize via various tools IDE plugin. TODO tools IDE plugins.<br>
At core most delivery pipelines will have some process to build code deploy code to various environments where apps get vetted before moved to higher environments. Identify the lowest environment where security tools can be embedded and how the various issues reported by tools be triaged, vetted and delivered to the app teams.<br>
in most cases it could a development environment where tools can be embedded and setup to create bug tickets for applications. (its important to tune the tools or you will need to add a additional triage layer to validate before sending to app teams)</p>
<h4 id="evaluate-and-identify-the-best-tools-for-your-stack-and-delivery-stream">Evaluate and identify the best tools for your stack and delivery stream</h4>
<h4 id="build-automation-to-integrate-the-tools-to-your-delivery-lifestyle-on-the-most-left-as-possible">Build automation to integrate the tools to your delivery lifestyle on the most left as possible</h4>
<p>Most of the popular tools have a lot of integration points with CI/CD tools. its important to invest in building automation to make it simple for new/existing application to get on-boarded.</p>
<h4 id="onboard-your-applications">Onboard your applications</h4>
<p>Onboard your application with this tools so the tools are scanning and running on your applications. This will ensure your security tasks and issues are identified and reported to the necessary members and team for action.</p>
<ul>
<li></li>
<li>SAST</li>
<li>IAST</li>
<li>OSS</li>
<li>Compliance</li>
<li>Threat Modeling</li>
</ul>
<p>All new and existing projects will be on boarded to a security automation platform that will listen to code checkin’s and runtime testing   on developer machine or lower environments we add listeners/webhooks that will listen to the changes in code/runtime and perform a variety of security checks in background using various <a href="https://ayalamanchili.github.io/security-testing-automation-tools.html">security testing automation tools and frameworks</a>. If a issue is found the its first sent to first response team to triage who will validate the issue which if is a valid finding will create a Bug for project team. This process typically happens with in ~4 hours from the moment the vulnerable code is checked in.<br>
As teams get notified with tickets with the needed details pertaining they can fix it and the Security orchestration will listen and run validated checks and if passed will close the issue and notify team.</p>
<h4 id="application-software">Application software</h4>
<p>All new and existing projects will be on boarded to a security automation platform that will</p>
<ul>
<li>listen to code changes 24 * 7 and initiate automated code scan with industry leading static application security testing tools that will run the scan to identify of vulnerabilities</li>
<li>If a issues are identified team are notified via email or ticket about the issue with in 1 hour of code changes.</li>
<li>teams will review and fix the issues and the automation will listen to the change hooks and re trigger a scan to validate them.</li>
<li>if the issue is fixed it will update the ticket and mark it closed or send a email.</li>
</ul>
<h4 id="rd-party-libraries-and-dependencies">3rd party libraries and dependencies</h4>
<ul>
<li>Any changes to the application dependencies triggers a scan of them using tools like depedency-checker, blackduck</li>
<li>if any issues are identified teams are notified via email or ticket</li>
</ul>

