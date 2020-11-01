---


---

<h1 id="lean-secure-software-delivery">Lean Secure Software Delivery</h1>
<h2 id="how-to-make-my-organization-dev-sec-ops-ready">How to make my organization dev-sec-ops ready?</h2>
<p>Lessons and best practices from years of work across  projects, teams and cultures pertaining to Lean secure software delivery.<br>
#ShiftLeft #SecureSDLC #DevSecOps</p>
<h3 id="before-state">Before State</h3>
<p>Security is a after thought and a necessary evil that software delivery teams have to deal with to release software/products.</p>
<ul>
<li>A manual process with help of tools to review applications and identify security issues.</li>
<li>Creating security bugs or tasks for high risk issues that need to be fixed before release.</li>
<li>Teams struggle to fix the issues leading to the expensive (time and money) sdlc cycle with most of the failing to release in time or releasing with accepted risk.</li>
<li>Most of the fixes end up creating substantial technical debt and effects code quality.</li>
<li>Most of the medium and low vulnerabilities end up in backlog and typically never looked at.</li>
<li>With growing pressure from business to release will end up creating risk tickets being accepted and vulnerable applications running in production.</li>
</ul>
<h3 id="current-state">Current State</h3>
<p>Security is integrated into the development life cycle from project initialization so security aspects are planned,implemented, identified and fixed early.  Essentially its ingrained into the day to day SDLC of teams.  This helps to made teams deliver secure software faster.</p>
<h3 id="how-can-you-get-there...">How can you get there…</h3>
<h4 id="review-your-software-delivery-workflow-and-identify-the-best-place-to-embed-security-tasks-and-issues.">Review your software delivery workflow and identify the best place to embed security tasks and issues.</h4>
<p>The best place to fix a bug is on a developers  machine before he commits this code. So this is good option and we should try to best utilize via various security <a href="https://ayalamanchili.github.io/secure-code-ide-plugins.html">IDE plugins</a>.</p>
<p>At core most delivery pipelines will have some process to build code deploy code to various environments where apps get vetted before moved to higher environments. Identify the lowest environment where security tools can be embedded and how the various issues reported by tools can be  triaged, vetted and delivered to the app teams, in most cases it could a development environment where tools can be embedded and setup to create bug tickets for applications.</p>
<blockquote>
<p>its important to tune the tools to minimize false positives to minimize noise to app teams  or you will need to add a additional triage layer to validate before sending to app teams</p>
</blockquote>
<h3 id="below-are-various-tool-categories-that-can-be-utilized.">Below are various tool categories that can be utilized.</h3>
<ul>
<li><a href="https://ayalamanchili.github.io/sast.html">SAST</a></li>
<li><a href="https://ayalamanchili.github.io/iast.html">IAST</a></li>
<li><a href="https://ayalamanchili.github.io/oss.html">OSS</a></li>
<li><a href="https://ayalamanchili.github.io/compliance-tools.html">Compliance</a></li>
<li><a href="https://ayalamanchili.github.io/treat-moedling.html">Treat Modeling</a></li>
<li><a href="https://ayalamanchili.github.io/web-scanners.html">Web Scanners</a></li>
</ul>
<h3 id="sample-sdlc-workflow-with-potential-best-phases-to-embed-your-security-tools.">Sample SDLC workflow with potential best phases to embed your security tools.</h3>
<p><img src="https://docs.google.com/drawings/d/e/2PACX-1vSZPaBFhSQrnUSqV8uiEOB2HVmzsO1p9Gc-7DFoNNGgmfcxA1JxReHFIlwd7dkhZi2bJ-iRsD3P9iJ0/pub?w=960&amp;h=720" alt="enter image description here"></p>
<h4 id="evaluate-and-identify-the-best-tools-for-your-stack-and-delivery-stream.">Evaluate and identify the best tools for your stack and delivery stream.</h4>
<p>Depending on your technology stack, skills, infrastructure setup identify the best tools that fit your deployment landscape.</p>
<h4 id="build-automation-to-integrate-the-tools-to-your-delivery-lifestyle-on-the-most-left-as-possible">Build automation to integrate the tools to your delivery lifestyle on the most left as possible</h4>
<p>Most of the popular tools have a lot of integration points with CI/CD tools. its important to invest in building automation to make it simple for new/existing application to get on-boarded.</p>
<h4 id="onboard-your-applications">Onboard your applications</h4>
<p>Onboard your application with this tools so the tools are scanning and running with your applications. This will ensure your security tasks and issues are identified and reported to the necessary members and team for action.</p>

