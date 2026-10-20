<!-- Keep this front matter at the very beginning of README.md. -->
<!-- Edit your biography, project links, and familiarity labels below. -->
<style>
/* GitHub Pages styling. Edit the text and links directly in this README. */
:root { --bg: #f6f7f4; --paper: #fff; --ink: #182b29; --muted: #526561; --accent: #137568; --line: #dce4df; --soft: #eaf3ed; }
html { scroll-behavior: smooth; scroll-padding-top: 24px; }
body { margin: 0; background: var(--bg); }
/* Primer supplies the document head; the README supplies the portfolio. */
.container-lg.markdown-body { max-width: 1160px; margin: 0 auto !important; padding: 0 40px !important; }
.markdown-body > h1:first-child, .markdown-body > .footer { display: none; }
.portfolio, .portfolio * { box-sizing: border-box; }
.portfolio { color: var(--ink); font: 16px/1.7 system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif; overflow-wrap: anywhere; }
.portfolio a { color: var(--accent); text-underline-offset: 4px; }
.portfolio a:hover { text-decoration: underline; }
.portfolio a:focus-visible { outline: 3px solid var(--accent); outline-offset: 5px; border-radius: 3px; }
.portfolio .topbar { display: flex; align-items: center; justify-content: space-between; gap: 24px; padding: 27px 0; border-bottom: 1px solid var(--line); }
.portfolio .brand { display: flex; align-items: center; gap: 12px; color: var(--ink); font-weight: 700; text-decoration: none; }
.portfolio .monogram { display: grid; place-items: center; width: 40px; height: 40px; border-radius: 12px; color: white; background: var(--accent); font-size: 14px; letter-spacing: .04em; }
.portfolio nav { display: flex; flex-wrap: wrap; gap: 25px; }
.portfolio nav a { color: var(--muted); font-size: 14px; font-weight: 600; text-decoration: none; }
.portfolio .hero { padding: 66px 0 55px; max-width: 870px; }
.portfolio .eyebrow { margin: 0 0 15px; color: var(--accent); font-size: 12px; font-weight: 750; text-transform: uppercase; letter-spacing: .14em; }
.portfolio h1, .portfolio h2, .portfolio h3 { color: var(--ink); border: 0; padding: 0; font-weight: 700; }
.portfolio h1 { font-size: clamp(36px, 4.8vw, 58px); line-height: 1.12; letter-spacing: -.045em; margin: 0 0 20px; max-width: 820px; }
.portfolio .role { font-size: 15px; color: var(--muted); margin: 0 0 20px; }
.portfolio .about { max-width: 755px; color: var(--muted); font-size: 17px; margin: 0 0 26px; }
.portfolio .actions { display: flex; flex-wrap: wrap; align-items: center; gap: 12px; }
.portfolio .button { display: inline-flex; align-items: center; justify-content: center; min-height: 44px; padding: 9px 18px; border: 1px solid var(--line); border-radius: 8px; color: var(--ink); background: var(--paper); font-size: 14px; font-weight: 650; text-decoration: none; }
.portfolio .button.primary { color: white; background: var(--accent); border-color: var(--accent); }
.portfolio .content { display: grid; grid-template-columns: minmax(0, 1fr) 294px; align-items: start; gap: 34px; padding-bottom: 66px; }
.portfolio .section-heading { display: flex; align-items: baseline; justify-content: space-between; gap: 15px; margin-bottom: 20px; }
.portfolio h2 { margin: 0; font-size: 23px; line-height: 1.3; letter-spacing: -.025em; }
.portfolio .count { color: var(--muted); font-size: 12px; letter-spacing: .08em; text-transform: uppercase; }
.portfolio .project { margin-bottom: 18px; padding: 27px 29px; background: var(--paper); border: 1px solid var(--line); border-radius: 14px; }
.portfolio .project:last-child { margin-bottom: 0; }
.portfolio .project .eyebrow { font-size: 10px; margin-bottom: 9px; }
.portfolio h3 { font-size: 23px; line-height: 1.3; letter-spacing: -.025em; margin: 0 0 12px; }
.portfolio .project p.description { margin: 0 0 17px; color: var(--muted); font-size: 15px; }
.portfolio ul.tags { display: flex; flex-wrap: wrap; gap: 7px; list-style: none; padding: 0; margin: 0 0 20px; }
.portfolio ul.tags li { margin: 0; background: var(--soft); border-radius: 5px; padding: 3px 9px; color: #34574c; font-size: 11px; font-weight: 600; }
.portfolio .project-links { display: flex; flex-wrap: wrap; gap: 12px 23px; }
.portfolio .project-links a { font-weight: 650; font-size: 13px; }
.portfolio .sidebar { margin-top: 50px; background: var(--paper); border: 1px solid var(--line); border-radius: 14px; padding: 26px 23px; }
.portfolio .sidebar h2 { font-size: 20px; }
.portfolio .sidebar-intro { font-size: 12px; color: var(--muted); margin: 10px 0 18px; }
.portfolio .language-list { margin: 0; padding: 0; }
.portfolio .language { display: flex; justify-content: space-between; gap: 12px; align-items: baseline; padding: 11px 0; border-bottom: 1px solid var(--line); }
.portfolio .language:last-child { border-bottom: 0; }
.portfolio .language dt { font-size: 13px; font-weight: 650; font-style: normal; padding: 0; margin: 0; }
.portfolio .language dd { padding: 0; margin: 0; text-align: right; font-size: 11px; color: var(--muted); }
.portfolio .sidebar-section { margin-top: 25px; padding-top: 22px; border-top: 1px solid var(--line); }
.portfolio .sidebar-section h3 { font-size: 13px; letter-spacing: 0; margin: 0 0 13px; }
.portfolio .sidebar .tags { gap: 6px; margin: 0; }
.portfolio .sidebar .tags li { font-size: 11px; background: var(--bg); color: var(--muted); }
.portfolio footer { border-top: 1px solid var(--line); padding: 25px 0; display: flex; justify-content: space-between; flex-wrap: wrap; gap: 12px; color: var(--muted); font-size: 12px; }
.portfolio footer p { margin: 0; }
@media (max-width: 800px) {
.container-lg.markdown-body { padding: 0 24px !important; }
.portfolio .content { grid-template-columns: minmax(0, 1fr); gap: 30px; }
.portfolio .sidebar { margin-top: 0; }
.portfolio .hero { padding: 47px 0 40px; }
}
@media (max-width: 480px) {
.container-lg.markdown-body { padding: 0 18px !important; }
.portfolio .topbar { flex-direction: column; align-items: flex-start; gap: 16px; padding: 21px 0; }
.portfolio nav { gap: 22px; }
.portfolio .project { padding: 24px 21px; }
.portfolio .section-heading { align-items: center; }
.portfolio .count { font-size: 10px; }
}
@media (prefers-reduced-motion: reduce) { html { scroll-behavior: auto; } }
</style>

<div class="portfolio" markdown="0">
<header class="topbar">
<a class="brand" href="#about">
<span class="monogram" aria-hidden="true">DC</span>
Dakota Chou
</a>
<nav aria-label="Main navigation">
<a href="#about">About</a>
<a href="#projects">Projects</a>
<a href="#languages">Languages</a>
</nav>
</header>
<main id="main">
<section id="about" class="hero" aria-labelledby="about-heading">
<p class="eyebrow">About me</p>
<h1 id="about-heading">Dakota Chou</h1>
<p class="role">Computer Science · Cal Poly San Luis Obispo</p>
<p class="about">I&#x27;m a computer science student at Cal Poly San Luis Obispo, graduating in May 2028. My work spans interactive VR experiences, community-focused web applications, and embedded navigation systems. I bring hands-on development experience and team leadership to projects that connect software with the way people learn, travel, and explore.</p>
<div class="actions">
<a class="button primary" href="https://github.com/kodychou">Explore my work <span aria-hidden="true">&nbsp;↘</span></a>
<a class="button" href="mailto:dakota_chou06@outlook.com">Get in touch</a>
<a class="button" href="https://www.linkedin.com/in/dakota-chou-011941272/">LinkedIn <span aria-hidden="true">&nbsp;↗</span></a>
</div>
</section>
<div class="content">
<section id="projects" aria-labelledby="projects-heading">
<div class="section-heading">
<h2 id="projects-heading">Selected projects</h2>
<span class="count">5 projects</span>
</div>
<article class="project" aria-labelledby="project-1">
<p class="eyebrow">Virtual reality · Education</p>
<h3 id="project-1">AeroSpace VR</h3>
<p class="description">An interactive VR game for the California Museum of Aerospace that introduces players of all ages to space exploration. I&#x27;m working in Unity with a team using an Agile workflow to build hands-on experiences that let players learn about and experience space.</p>
<ul class="tags" aria-label="Technologies and focus areas">
<li>Unity</li>
<li>C#</li>
<li>VR</li>
<li>Agile</li>
</ul>
<div class="project-links">
<a href="https://laes.calpoly.edu/Aerospace-VR">About the project <span aria-hidden="true">↗</span></a>
</div>
</article>
<article class="project" aria-labelledby="project-2">
<p class="eyebrow">Web development · Team leadership</p>
<h3 id="project-2">PolyPool.org</h3>
<p class="description">A carpooling platform that helps Cal Poly students find rides across California. I lead a team of two other programmers building the site, including Google Maps integration to calculate and visualize routes.</p>
<ul class="tags" aria-label="Technologies and focus areas">
<li>JavaScript</li>
<li>React</li>
<li>Express</li>
<li>Google Maps API</li>
</ul>
<div class="project-links">
<a href="https://polypool.org" aria-label="View project: PolyPool.org">View project <span aria-hidden="true">↗</span></a>
</div>
</article>
<article class="project" aria-labelledby="project-3">
<p class="eyebrow">Robotics · Embedded systems</p>
<h3 id="project-3">BIERfish Navigation</h3>
<p class="description">Navigation and control software for a free-swimming robotic fish, developed during my internship with the University of Virginia&#x27;s BIER Lab. I used Python and C++ for marker-relative navigation, motor control, and onboard sensor data collection, enabling the robot to navigate around obstacles toward a goal.</p>
<ul class="tags" aria-label="Technologies and focus areas">
<li>Python</li>
<li>C++</li>
<li>Motor control</li>
<li>Sensor integration</li>
</ul>
<div class="project-links">
<a href="https://cpslo-my.sharepoint.com/:b:/r/personal/dbchou_calpoly_edu/Documents/Navigation%20Recap.pdf?d=wbccfec373f4346fc87d45068c47fca3a&csf=1&web=1&e=h0KwTi">Learn More <span aria-hidden="true">↗</span></a>
</div>
</article>
<article class="project" aria-labelledby="project-4">
<p class="eyebrow">Game development</p>
<h3 id="project-4">Bank Heist Game</h3>
<p class="description">A game I created that challenges players to navigate a bank, steal as much money as possible, and escape without getting caught. Each run asks players to balance a bigger payout against the risk of detection.</p>
<ul class="tags" aria-label="Technologies and focus areas">
<li>Game development</li>
<li>Gameplay systems</li>
</ul>
<div class="project-links">
<a href="https://kodychou.itch.io/bank-heist" aria-label="Ask about Bank Heist Game">Ask about this project <span aria-hidden="true">↗</span></a>
</div>
</article>
<article class="project" aria-labelledby="project-5">
<p class="eyebrow">More to explore</p>
<h3 id="project-5">Other Projects</h3>
<p class="description">More programming projects and experiments. Get in touch to learn about additional work, or browse the collection when a link is available.</p>
<div class="project-links">
<a href="mailto:dakota_chou06@outlook.com?subject=Other+Projects" aria-label="Ask about Other Projects">Ask about my other projects <span aria-hidden="true">↗</span></a>
</div>
</article>
</section>
<aside id="languages" class="sidebar" aria-labelledby="languages-heading">
<h2 id="languages-heading">Languages</h2>
<p class="sidebar-intro">My experience at a glance.</p>
<dl class="language-list">
<div class="language">
<dt>C#</dt>
<dd>Project experience</dd>
</div>
<div class="language">
<dt>Python</dt>
<dd>Project experience</dd>
</div>
<div class="language">
<dt>C++</dt>
<dd>Project experience</dd>
</div>
<div class="language">
<dt>JavaScript</dt>
<dd>Project experience</dd>
</div>
<div class="language">
<dt>TypeScript</dt>
<dd>Familiar</dd>
</div>
<div class="language">
<dt>C</dt>
<dd>Familiar</dd>
</div>
<div class="language">
<dt>Java</dt>
<dd>Familiar</dd>
</div>
<div class="language">
<dt>Swift</dt>
<dd>Familiar</dd>
</div>
<div class="language">
<dt>Assembly</dt>
<dd>Familiar</dd>
</div>
</dl>
<section class="sidebar-section" aria-labelledby="web-heading">
<h3 id="web-heading">Web technologies</h3>
<ul class="tags">
<li>HTML</li>
<li>React</li>
<li>Express</li>
</ul>
</section>
<section class="sidebar-section" aria-labelledby="tools-heading">
<h3 id="tools-heading">Tools &amp; platforms</h3>
<ul class="tags">
<li>Unity</li>
<li>Git</li>
<li>Figma</li>
<li>Xcode</li>
<li>VS Code</li>
<li>Arduino</li>
<li>Raspberry Pi</li>
</ul>
</section>
</aside>
</div>
</main>
<footer>
<p>© Dakota Chou</p>
<a href="mailto:dakota_chou06@outlook.com">Let's connect <span aria-hidden="true">↗</span></a>
</footer>
</div>
