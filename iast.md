---


---

<h1 id="iast">IAST</h1>
<p>Process of instrumenting runtime code to identify and report security vulnerabilities.</p>
<h2 id="how-to-integrate">How to integrate</h2>
<ul>
<li>
<p>IAST client agents should be initialized during application startup<br>
so they can instrument runtime code to detect and report security<br>
issues to central IAST server</p>
</li>
<li>
<p>IAST tools can be configured to report issues directly to application ticketing systems to manage and remediate security issues</p>
</li>
<li></li>
</ul>
<h2 id="iast-tools">IAST Tools</h2>
<h3 id="pros">Pros</h3>
<ul>
<li>less false positives since it instrument runtime code</li>
</ul>
<h3 id="cons">Cons</h3>
<ul>
<li>add minor performance impact.</li>
</ul>

