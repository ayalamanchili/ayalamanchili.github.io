---


---

<h1 id="lean-secure-software-delivery">Lean Secure Software Delivery</h1>
<p>I am going to share some lessons and best practices from years of work across projects, teams and cultures pertaining to software delivery and security.</p>
<h3 id="before-state">Before State</h3>
<p>Security is a after thought and necessary evil that software delivery teams have to deal with to release software/products.</p>
<ul>
<li>A manual/automated process to review (via SAST tools) the software code identifying the vulnerabilities in code that was build and tested sometime back.</li>
<li>Creating security bugs or tasks for high risk issues that need to be fixed before release.</li>
<li>Teams struggle to fix the issues leading to the expensive (time and money) sdlc cycle with most of the failing to release in time.</li>
<li>Most of the fixes end up creating substantial technical debt and effects code quality.</li>
<li>Most of the medium and low vulnerabilities end up in backlog and typically never looked at.</li>
<li>With growing pressure from business to release will end up creating risk tickets being accepted.</li>
</ul>
<h3 id="current-state">Current State</h3>
<p>Security is integrated into the development life cycle from project initialization and any issues are identified and fixed at inception.  This helps to made teams deliver secure software faster.<br>
#ShiftLeft #SecureSDLC</p>
<h3 id="how-did-we-get-there">How did we get there?</h3>
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
<blockquote>
<p><strong>Note:</strong> The <strong>Publish now</strong> button is disabled if your file has not been published yet.</p>
</blockquote>
<h2 id="manage-file-publication">Manage file publication</h2>
<p>Since one file can be published to multiple locations, you can list and manage publish locations by clicking <strong>File publication</strong> in the <strong>Publish</strong> sub-menu. This allows you to list and remove publication locations that are linked to your file.</p>
<h1 id="markdown-extensions">Markdown extensions</h1>
<p>StackEdit extends the standard Markdown syntax by adding extra <strong>Markdown extensions</strong>, providing you with some nice features.</p>
<blockquote>
<p><strong>ProTip:</strong> You can disable any <strong>Markdown extension</strong> in the <strong>File properties</strong> dialog.</p>
</blockquote>
<h2 id="smartypants">SmartyPants</h2>
<p>SmartyPants converts ASCII punctuation characters into “smart” typographic punctuation HTML entities. For example:</p>

<table>
<thead>
<tr>
<th></th>
<th>ASCII</th>
<th>HTML</th>
</tr>
</thead>
<tbody>
<tr>
<td>Single backticks</td>
<td><code>'Isn't this fun?'</code></td>
<td>‘Isn’t this fun?’</td>
</tr>
<tr>
<td>Quotes</td>
<td><code>"Isn't this fun?"</code></td>
<td>“Isn’t this fun?”</td>
</tr>
<tr>
<td>Dashes</td>
<td><code>-- is en-dash, --- is em-dash</code></td>
<td>– is en-dash, — is em-dash</td>
</tr>
</tbody>
</table><h2 id="uml-diagrams">UML diagrams</h2>
<p>You can render UML diagrams using <a href="https://mermaidjs.github.io/">Mermaid</a>. For example, this will produce a sequence diagram:</p>
<div class="mermaid"><svg xmlns="http://www.w3.org/2000/svg" id="mermaid-svg-SRo3KkrQ4rhz671n" height="100%" width="100%" style="max-width:750px;" viewBox="-50 -10 750 457"><g></g><g><line id="actor18" x1="75" y1="5" x2="75" y2="446" class="actor-line" stroke-width="0.5px" stroke="#999"></line><rect x="0" y="0" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="75" y="32.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="75" dy="0">Alice</tspan></text></g><g><line id="actor19" x1="275" y1="5" x2="275" y2="446" class="actor-line" stroke-width="0.5px" stroke="#999"></line><rect x="200" y="0" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="275" y="32.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="275" dy="0">Bob</tspan></text></g><g><line id="actor20" x1="475" y1="5" x2="475" y2="446" class="actor-line" stroke-width="0.5px" stroke="#999"></line><rect x="400" y="0" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="475" y="32.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="475" dy="0">John</tspan></text></g><defs><marker id="arrowhead" refX="5" refY="2" markerWidth="6" markerHeight="4" orient="auto"><path d="M 0,0 V 4 L6,2 Z"></path></marker></defs><defs><marker id="crosshead" markerWidth="15" markerHeight="8" orient="auto" refX="16" refY="4"><path fill="black" stroke="#000000" stroke-width="1px" d="M 9,2 V 6 L16,4 Z" style="stroke-dasharray: 0, 0;"></path><path fill="none" stroke="#000000" stroke-width="1px" d="M 0,1 L 6,7 M 6,1 L 0,7" style="stroke-dasharray: 0, 0;"></path></marker></defs><g><text x="175" y="93" class="messageText" style="text-anchor: middle;">Hello Bob, how are you?</text><line x1="75" y1="100" x2="275" y2="100" class="messageLine0" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="fill: none;"></line></g><g><text x="375" y="128" class="messageText" style="text-anchor: middle;">How about you John?</text><line x1="275" y1="135" x2="475" y2="135" class="messageLine1" stroke-width="2" stroke="black" marker-end="url(#arrowhead)" style="stroke-dasharray: 3, 3; fill: none;"></line></g><g><text x="175" y="163" class="messageText" style="text-anchor: middle;">I am good thanks!</text><line x1="275" y1="170" x2="75" y2="170" class="messageLine1" stroke-width="2" stroke="black" marker-end="url(#crosshead)" style="stroke-dasharray: 3, 3; fill: none;"></line></g><g><text x="375" y="198" class="messageText" style="text-anchor: middle;">I am good thanks!</text><line x1="275" y1="205" x2="475" y2="205" class="messageLine0" stroke-width="2" stroke="black" marker-end="url(#crosshead)" style="fill: none;"></line></g><g><rect x="500" y="215" fill="#EDF2AE" stroke="#666" width="150" height="76" rx="0" ry="0" class="note"></rect><text x="496" y="239" fill="black" class="noteText"><tspan x="516" fill="black">Bob thinks a long</tspan></text><text x="496" y="253" fill="black" class="noteText"><tspan x="516" fill="black">long time, so long</tspan></text><text x="496" y="267" fill="black" class="noteText"><tspan x="516" fill="black">that the text does</tspan></text><text x="496" y="281" fill="black" class="noteText"><tspan x="516" fill="black">not fit on a row.</tspan></text></g><g><text x="175" y="319" class="messageText" style="text-anchor: middle;">Checking with John...</text><line x1="275" y1="326" x2="75" y2="326" class="messageLine1" stroke-width="2" stroke="black" style="stroke-dasharray: 3, 3; fill: none;"></line></g><g><text x="275" y="354" class="messageText" style="text-anchor: middle;">Yes... John, how are you?</text><line x1="75" y1="361" x2="475" y2="361" class="messageLine0" stroke-width="2" stroke="black" style="fill: none;"></line></g><g><rect x="0" y="381" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="75" y="413.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="75" dy="0">Alice</tspan></text></g><g><rect x="200" y="381" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="275" y="413.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="275" dy="0">Bob</tspan></text></g><g><rect x="400" y="381" fill="#eaeaea" stroke="#666" width="150" height="65" rx="3" ry="3" class="actor"></rect><text x="475" y="413.5" dominant-baseline="central" alignment-baseline="central" class="actor" style="text-anchor: middle;"><tspan x="475" dy="0">John</tspan></text></g></svg></div>
<p>And this will produce a flow chart:</p>
<div class="mermaid"><svg xmlns="http://www.w3.org/2000/svg" id="mermaid-svg-cgovTazujsw3vHuv" width="100%" style="max-width: 727.4296875px;" viewBox="0 0 727.4296875 199.4296875"><g transform="translate(-12, -12)"><g class="output"><g class="clusters"></g><g class="edgePaths"><g class="edgePath" style="opacity: 1;"><path class="path" d="M117.109375,130.2492274291304L211.3125,94.21484375L305.515625,94.21484375" marker-end="url(#arrowhead183)" style="fill:none"></path><defs><marker id="arrowhead183" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M644.2562781662434,171.822265625L593.8046875,203.4296875L482.88671875,203.4296875L383.671875,203.4296875L332.09375,203.4296875L211.3125,203.4296875L117.109375,167.3953038208696" marker-end="url(#arrowhead184)" style="fill:none"></path><defs><marker id="arrowhead184" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M358.671875,94.21484375L383.671875,94.21484375L409.171875,94.71484375" marker-end="url(#arrowhead185)" style="fill:none"></path><defs><marker id="arrowhead185" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath" style="opacity: 1;"><path class="path" d="M557.6015625,94.71484375L593.8046875,94.21484375L644.2562781662434,125.822265625" marker-end="url(#arrowhead186)" style="fill:none"></path><defs><marker id="arrowhead186" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g></g><g class="edgeLabels"><g class="edgeLabel" transform="translate(211.3125,94.21484375)" style="opacity: 1;"><g transform="translate(-69.203125,-13)" class="label"><foreignObject width="138.40625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">code change trigger</span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel"></span></div></foreignObject></g></g><g class="edgeLabel" transform="translate(593.8046875,94.21484375)" style="opacity: 1;"><g transform="translate(-11.703125,-13)" class="label"><foreignObject width="23.40625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span class="edgeLabel">yes</span></div></foreignObject></g></g></g><g class="nodes"><g class="node" id="A" transform="translate(68.5546875,148.822265625)" style="opacity: 1;"><rect rx="0" ry="0" x="-48.5546875" y="-23" width="97.109375" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-38.5546875,-13)"><foreignObject width="77.109375" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Code Repo</div></foreignObject></g></g></g><g class="node" id="B" transform="translate(332.09375,94.21484375)" style="opacity: 1;"><circle x="-26.578125" y="-23" r="26.578125"></circle><g class="label" transform="translate(0,0)"><g transform="translate(-16.578125,-13)"><foreignObject width="33.15625" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Scan</div></foreignObject></g></g></g><g class="node" id="C" transform="translate(680.96875,148.822265625)" style="opacity: 1;"><rect rx="0" ry="0" x="-50.4609375" y="-23" width="100.921875" height="46"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-40.4609375,-13)"><foreignObject width="80.921875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">notify team</div></foreignObject></g></g></g><g class="node" id="D" transform="translate(482.88671875,94.21484375)" style="opacity: 1;"><polygon points="74.21484375,0 148.4296875,-74.21484375 74.21484375,-148.4296875 0,-74.21484375" rx="5" ry="5" transform="translate(-74.21484375,74.21484375)"></polygon><g class="label" transform="translate(0,0)"><g transform="translate(-49.4609375,-13)"><foreignObject width="98.921875" height="26"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">has any issues</div></foreignObject></g></g></g></g></g></g></svg></div>

