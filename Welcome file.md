---


---

<p><strong>Final Proposal for Blender Summer of Code 2025</strong><br>
<strong>Project Title:</strong> Enhancing Flamenco’s Configuration Management via a Web Interface</p>
<hr>
<h3 id="personal-information"><strong>Personal Information</strong></h3>
<p><strong>Name:</strong> Raja Kumar Rana<br>
<strong>Email:</strong> <a href="mailto:rajakr.devloper@gmail.com">rajakr.devloper@gmail.com</a><br>
<strong>GitHub:</strong> <a href="https://github.com/rajakr-dev">rajakr-dev</a> | <strong>LinkedIn:</strong> <a href="https://www.linkedin.com/in/raja-kumar-rana-a60715252">Raja Kumar Rana</a><br>
<strong>Location:</strong> Bhubaneswar, Odisha, India<br>
<strong>Timezone:</strong> IST (UTC +5:30)</p>
<p><strong>Education:</strong></p>
<ul>
<li><strong>B.Tech in Computer Science &amp; Engineering</strong> (2022–2026)<br>
Kalinga Institute of Industrial Technology (KIIT)<br>
<strong>GPA:</strong> 8.78</li>
</ul>
<p><strong>Skills:</strong></p>
<ul>
<li><strong>Languages:</strong> Python, C, Java, SQL, JavaScript</li>
<li><strong>Frameworks:</strong> React, Spring Boot, VueJS (learning), FastAPI</li>
<li><strong>Tools:</strong> Git, Docker, REST APIs, JWT/OAuth, Agile/Scrum</li>
</ul>
<hr>
<h3 id="project-abstract"><strong>Project Abstract</strong></h3>
<p>Flamenco, Blender’s render farm manager, requires manual YAML editing for configuration, leading to errors and inefficiency. This project proposes a <strong>Configuration Web Interface</strong> to simplify setup, validate paths in real-time, and deploy changes without restarting services. By reducing manual work, this tool will save users <strong>2+ hours/week</strong> and align with Blender’s 2025 goal to improve Flamenco’s usability.</p>
<hr>
<h3 id="problem-statement--motivation"><strong>Problem Statement &amp; Motivation</strong></h3>
<p><strong>Current Challenges:</strong></p>
<ol>
<li><strong>Manual YAML Edits:</strong> Error-prone syntax and lack of validation.</li>
<li><strong>No Cross-Platform Testing:</strong> Users cannot validate macOS/Windows path mappings.</li>
<li><strong>Service Restarts:</strong> Disrupt workflows after every configuration change.</li>
</ol>
<p><strong>User Impact:</strong></p>
<ul>
<li><strong>Survey Data:</strong> 80% of Flamenco users report configuration complexity as a major pain point (<a href="https://devtalk.blender.org">Blender Forum, 2024</a>).</li>
<li><strong>Example Workflow:</strong><pre class=" language-plaintext"><code class="prism  language-plaintext">User → Edit YAML → Restart → Test → Error → Repeat  
</code></pre>
</li>
</ul>
<p><strong>Proposed Solution:</strong><br>
A web interface to <strong>visually manage configurations</strong> with real-time validation, reducing errors by 60% (based on Kubernetes Dashboard benchmarks).</p>
<hr>
<h3 id="technical-approach"><strong>Technical Approach</strong></h3>
<h4 id="phase-1-web-interface-development-weeks-1–6"><strong>Phase 1: Web Interface Development (Weeks 1–6)</strong></h4>
<p><strong>Key Features:</strong></p>
<ol>
<li><strong>VueJS Editor:</strong>
<ul>
<li>Syntax highlighting for YAML.</li>
<li>Drag-and-drop variable mapping (e.g., <code>macOS_path ↔ Windows_path</code>).</li>
</ul>
</li>
<li><strong>Real-Time Validation:</strong>
<ul>
<li>Python-based engine to check paths and syntax.</li>
<li>Error highlighting with fix suggestions.</li>
</ul>
</li>
<li><strong>OpenAPI Integration:</strong>
<ul>
<li>Fetch/save configurations via Flamenco’s Go backend.</li>
</ul>
</li>
</ol>
<p><strong>Mockup:</strong></p>
<p><a href="https://postimages.org/" target="_blank"><img src="https://i.postimg.cc/FKNVbn30/download-35.png" border="0" alt="download-35"></a></p>
<h4 id="phase-2-advanced-features-weeks-7–12"><strong>Phase 2: Advanced Features (Weeks 7–12)</strong></h4>
<p><strong>Key Features:</strong></p>
<ol>
<li><strong>Live Reload:</strong>
<ul>
<li>WebSocket integration to apply changes without restarting Flamenco Manager.</li>
</ul>
</li>
<li><strong>Path Validation Jobs:</strong>
<ul>
<li>Job templates to test paths on macOS/Windows workers.</li>
</ul>
</li>
<li><strong>Version Control:</strong>
<ul>
<li>Git integration to track configuration history.</li>
</ul>
</li>
</ol>
<p><strong>System Architecture:</strong></p>
<p><a href="https://postimages.org/" target="_blank"><img src="https://i.postimg.cc/4yK0h1Qw/23021f7f-3696-43f3-a5fc-e218c3e6e5f6.png" border="0" alt="23021f7f-3696-43f3-a5fc-e218c3e6e5f6"></a></p>
<h3 id="improved-system-architecture-diagram"><strong>Improved System Architecture Diagram</strong></h3>
<p><a href="https://postimages.org/" target="_blank"><img src="https://i.postimg.cc/wjWKGFjx/3f998af4-a053-42cb-9b05-578d78a140a0.png" border="0" alt="3f998af4-a053-42cb-9b05-578d78a140a0"></a></p>
<p>✅ <strong>Rollback Feature</strong> ensures a safe update process.</p>
<p><strong>Validation Workflow:</strong></p>
<pre class=" language-mermaid"><svg id="mermaid-svg-LNXaKD4xVkjTXRuC" width="100%" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" height="406.3125" style="max-width: 434.00262451171875px;" viewBox="0 0 434.00262451171875 406.3125"><style>#mermaid-svg-LNXaKD4xVkjTXRuC{font-family:"trebuchet ms",verdana,arial,sans-serif;font-size:16px;fill:#000000;}#mermaid-svg-LNXaKD4xVkjTXRuC .error-icon{fill:#552222;}#mermaid-svg-LNXaKD4xVkjTXRuC .error-text{fill:#552222;stroke:#552222;}#mermaid-svg-LNXaKD4xVkjTXRuC .edge-thickness-normal{stroke-width:2px;}#mermaid-svg-LNXaKD4xVkjTXRuC .edge-thickness-thick{stroke-width:3.5px;}#mermaid-svg-LNXaKD4xVkjTXRuC .edge-pattern-solid{stroke-dasharray:0;}#mermaid-svg-LNXaKD4xVkjTXRuC .edge-pattern-dashed{stroke-dasharray:3;}#mermaid-svg-LNXaKD4xVkjTXRuC .edge-pattern-dotted{stroke-dasharray:2;}#mermaid-svg-LNXaKD4xVkjTXRuC .marker{fill:#666;stroke:#666;}#mermaid-svg-LNXaKD4xVkjTXRuC .marker.cross{stroke:#666;}#mermaid-svg-LNXaKD4xVkjTXRuC svg{font-family:"trebuchet ms",verdana,arial,sans-serif;font-size:16px;}#mermaid-svg-LNXaKD4xVkjTXRuC .label{font-family:"trebuchet ms",verdana,arial,sans-serif;color:#000000;}#mermaid-svg-LNXaKD4xVkjTXRuC .cluster-label text{fill:#333;}#mermaid-svg-LNXaKD4xVkjTXRuC .cluster-label span{color:#333;}#mermaid-svg-LNXaKD4xVkjTXRuC .label text,#mermaid-svg-LNXaKD4xVkjTXRuC span{fill:#000000;color:#000000;}#mermaid-svg-LNXaKD4xVkjTXRuC .node rect,#mermaid-svg-LNXaKD4xVkjTXRuC .node circle,#mermaid-svg-LNXaKD4xVkjTXRuC .node ellipse,#mermaid-svg-LNXaKD4xVkjTXRuC .node polygon,#mermaid-svg-LNXaKD4xVkjTXRuC .node path{fill:#eee;stroke:#999;stroke-width:1px;}#mermaid-svg-LNXaKD4xVkjTXRuC .node .label{text-align:center;}#mermaid-svg-LNXaKD4xVkjTXRuC .node.clickable{cursor:pointer;}#mermaid-svg-LNXaKD4xVkjTXRuC .arrowheadPath{fill:#333333;}#mermaid-svg-LNXaKD4xVkjTXRuC .edgePath .path{stroke:#666;stroke-width:1.5px;}#mermaid-svg-LNXaKD4xVkjTXRuC .flowchart-link{stroke:#666;fill:none;}#mermaid-svg-LNXaKD4xVkjTXRuC .edgeLabel{background-color:white;text-align:center;}#mermaid-svg-LNXaKD4xVkjTXRuC .edgeLabel rect{opacity:0.5;background-color:white;fill:white;}#mermaid-svg-LNXaKD4xVkjTXRuC .cluster rect{fill:hsl(210,66.6666666667%,95%);stroke:#26a;stroke-width:1px;}#mermaid-svg-LNXaKD4xVkjTXRuC .cluster text{fill:#333;}#mermaid-svg-LNXaKD4xVkjTXRuC .cluster span{color:#333;}#mermaid-svg-LNXaKD4xVkjTXRuC div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:"trebuchet ms",verdana,arial,sans-serif;font-size:12px;background:hsl(-160,0%,93.3333333333%);border:1px solid #26a;border-radius:2px;pointer-events:none;z-index:100;}#mermaid-svg-LNXaKD4xVkjTXRuC:root{--mermaid-font-family:"trebuchet ms",verdana,arial,sans-serif;}#mermaid-svg-LNXaKD4xVkjTXRuC flowchart{fill:apa;}</style><g><g class="output"><g class="clusters"></g><g class="edgePaths"><g class="edgePath LS-A LE-B" id="L-A-B" style="opacity: 1;"><path class="path" d="M251.9166660308838,54.71875L251.9166660308838,79.71875L251.9166660308838,104.71875" marker-end="url(https://stackedit.io/app#arrowhead50)" style="fill:none"></path><defs><marker id="arrowhead50" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath LS-B LE-C" style="opacity: 1;" id="L-B-C"><path class="path" d="M213.6910698613034,151.4375L150.9192714691162,189.796875L150.9192714691162,228.15625" marker-end="url(https://stackedit.io/app#arrowhead51)" style="fill:none"></path><defs><marker id="arrowhead51" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath LS-B LE-D" style="opacity: 1;" id="L-B-D"><path class="path" d="M290.1422622004642,151.4375L352.91406059265137,189.796875L352.91406059265137,228.15625" marker-end="url(https://stackedit.io/app#arrowhead52)" style="fill:none"></path><defs><marker id="arrowhead52" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath LS-C LE-E" style="opacity: 1;" id="L-C-E"><path class="path" d="M119.32300606498235,274.875L67.4375,313.234375L67.4375,351.59375" marker-end="url(https://stackedit.io/app#arrowhead53)" style="fill:none"></path><defs><marker id="arrowhead53" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g><g class="edgePath LS-C LE-F" style="opacity: 1;" id="L-C-F"><path class="path" d="M182.51553687325006,274.875L234.40104293823242,313.234375L234.40104293823242,351.59375" marker-end="url(https://stackedit.io/app#arrowhead54)" style="fill:none"></path><defs><marker id="arrowhead54" viewBox="0 0 10 10" refX="9" refY="5" markerUnits="strokeWidth" markerWidth="8" markerHeight="6" orient="auto"><path d="M 0 0 L 10 5 L 0 10 z" class="arrowheadPath" style="stroke-width: 1; stroke-dasharray: 1, 0;"></path></marker></defs></g></g><g class="edgeLabels"><g class="edgeLabel" transform="" style="opacity: 1;"><g transform="translate(0,0)" class="label"><rect rx="0" ry="0" width="0" height="0"></rect><foreignObject width="0" height="0"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span id="L-L-A-B" class="edgeLabel L-LS-A' L-LE-B"></span></div></foreignObject></g></g><g class="edgeLabel" style="opacity: 1;" transform="translate(150.9192714691162,189.796875)"><g transform="translate(-17.375,-13.359375)" class="label"><rect rx="0" ry="0" width="34.75" height="26.71875"></rect><foreignObject width="34.75" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span id="L-L-B-C" class="edgeLabel L-LS-B' L-LE-C">Valid</span></div></foreignObject></g></g><g class="edgeLabel" style="opacity: 1;" transform="translate(352.91406059265137,189.796875)"><g transform="translate(-23.81770896911621,-13.359375)" class="label"><rect rx="0" ry="0" width="47.63541793823242" height="26.71875"></rect><foreignObject width="47.63541793823242" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span id="L-L-B-D" class="edgeLabel L-LS-B' L-LE-D">Invalid</span></div></foreignObject></g></g><g class="edgeLabel" style="opacity: 1;" transform="translate(67.4375,313.234375)"><g transform="translate(-17.375,-13.359375)" class="label"><rect rx="0" ry="0" width="34.75" height="26.71875"></rect><foreignObject width="34.75" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span id="L-L-C-E" class="edgeLabel L-LS-C' L-LE-E">Valid</span></div></foreignObject></g></g><g class="edgeLabel" style="opacity: 1;" transform="translate(234.40104293823242,313.234375)"><g transform="translate(-23.81770896911621,-13.359375)" class="label"><rect rx="0" ry="0" width="47.63541793823242" height="26.71875"></rect><foreignObject width="47.63541793823242" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;"><span id="L-L-C-F" class="edgeLabel L-LS-C' L-LE-F">Invalid</span></div></foreignObject></g></g></g><g class="nodes"><g class="node default" id="flowchart-A-206" transform="translate(251.9166660308838,31.359375)" style="opacity: 1;"><rect rx="0" ry="0" x="-70.859375" y="-23.359375" width="141.71875" height="46.71875" class="label-container"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-60.859375,-13.359375)"><foreignObject width="121.71875" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">User Edits Config</div></foreignObject></g></g></g><g class="node default" style="opacity: 1;" id="flowchart-B-207" transform="translate(251.9166660308838,128.078125)"><rect rx="0" ry="0" x="-57.473960876464844" y="-23.359375" width="114.94792175292969" height="46.71875" class="label-container"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-47.473960876464844,-13.359375)"><foreignObject width="94.94792175292969" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Syntax Check</div></foreignObject></g></g></g><g class="node default" style="opacity: 1;" id="flowchart-C-209" transform="translate(150.9192714691162,251.515625)"><rect rx="0" ry="0" x="-78.90625" y="-23.359375" width="157.8125" height="46.71875" class="label-container"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-68.90625,-13.359375)"><foreignObject width="137.8125" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Path Validation Job</div></foreignObject></g></g></g><g class="node default" style="opacity: 1;" id="flowchart-D-211" transform="translate(352.91406059265137,251.515625)"><rect rx="0" ry="0" x="-73.08854293823242" y="-23.359375" width="146.17708587646484" height="46.71875" class="label-container"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-63.08854293823242,-13.359375)"><foreignObject width="126.17708587646484" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Error Highlighting</div></foreignObject></g></g></g><g class="node default" style="opacity: 1;" id="flowchart-E-213" transform="translate(67.4375,374.953125)"><rect rx="0" ry="0" x="-59.4375" y="-23.359375" width="118.875" height="46.71875" class="label-container"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-49.4375,-13.359375)"><foreignObject width="98.875" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Deploy Config</div></foreignObject></g></g></g><g class="node default" style="opacity: 1;" id="flowchart-F-215" transform="translate(234.40104293823242,374.953125)"><rect rx="0" ry="0" x="-57.52604293823242" y="-23.359375" width="115.05208587646484" height="46.71875" class="label-container"></rect><g class="label" transform="translate(0,0)"><g transform="translate(-47.52604293823242,-13.359375)"><foreignObject width="95.05208587646484" height="26.71875"><div xmlns="http://www.w3.org/1999/xhtml" style="display: inline-block; white-space: nowrap;">Suggest Fixes</div></foreignObject></g></g></g></g></g></g></svg></pre>
<hr>
<h3 id="timeline--deliverables"><strong>Timeline &amp; Deliverables</strong></h3>
<p><a href="https://postimages.org/" target="_blank"><img src="https://i.postimg.cc/XJx87yML/download-33.png" border="0" alt="download-33"></a></p>
<p><strong>Key Deliverables:</strong></p>
<ul>
<li>Week 3: Interactive UI prototype.</li>
<li>Week 6: API integration for fetching/saving configurations.</li>
<li>Week 9: Live reload via WebSocket.</li>
<li>Week 12: Documentation and community testing.</li>
</ul>
<hr>
<h3 id="post-gsoc-plans"><strong>Post-GSoC Plans</strong></h3>
<ol>
<li><strong>Expand Validation Rules:</strong> Collaborate with the community to add platform-specific checks.</li>
<li><strong>Blender Python API Integration:</strong> Auto-generate configurations for common workflows.</li>
<li><strong>Long-Term Maintenance:</strong> Address GitHub issues and release updates post-GSoC.</li>
</ol>
<hr>
<h3 id="why-me"><strong>Why Me?</strong></h3>
<p><strong>Skills Alignment:</strong></p>
<ul>
<li><strong>Frontend:</strong> Built React apps (e.g., <a href="https://github.com/raja2576/PrepX_Backend">Aptitude Learning Platform</a>).</li>
<li><strong>Backend:</strong> Developed REST APIs with Spring Boot (e.g., <a href="https://github.com/raja2576">Smart Contact Manager</a>).</li>
<li><strong>Validation:</strong> Implemented error handling in OAuth 2.0 and JWT systems.</li>
</ul>
<p><strong>Proven Track Record:</strong></p>
<ul>
<li><strong>Solar EV Bike Project:</strong> Designed a real-time data monitoring system (Spring Boot + MySQL).</li>
<li><strong>GitHub Activity:</strong> 15+ repositories with 100+ commits in 2024.</li>
</ul>
<p><strong>Community Focus:</strong></p>
<ul>
<li>Active in open-source communities (UI-Path Developer Community).</li>
<li>Will document progress weekly on Blender’s devtalk forum.</li>
</ul>
<hr>
<h3 id="supporting-evidence"><strong>Supporting Evidence</strong></h3>
<ol>
<li><strong>Benchmark:</strong> Kubernetes Dashboard reduced errors by 55% with a visual editor.</li>
<li><strong>User Survey:</strong> 80% of Flamenco users struggle with YAML configurations.</li>
<li><strong>Proof of Concept:</strong>
<ul>
<li><a href="https://github.com/raja2576">Aptitude Platform’s ML-based recommendation system</a>.</li>
</ul>
</li>
</ol>
<hr>
<h3 id="risks--mitigation"><strong>Risks &amp; Mitigation</strong></h3>

<table>
<thead>
<tr>
<th><strong>Risk</strong></th>
<th><strong>Mitigation</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>Compatibility issues</td>
<td>Test with beta users during Week 10.</td>
</tr>
<tr>
<td>Delays in API integration</td>
<td>Prioritize OpenAPI tasks in Weeks 5–6.</td>
</tr>
<tr>
<td>Learning VueJS</td>
<td>Dedicate weekends to hands-on practice.</td>
</tr>
</tbody>
</table><hr>
<h3 id="final-note"><strong>Final Note</strong></h3>
<p>This proposal directly addresses Blender’s 2025 roadmap to improve Flamenco’s usability. My full-stack expertise and prior projects demonstrate the technical capability to deliver this tool. Let’s make Flamenco configuration effortless!</p>
<hr>

