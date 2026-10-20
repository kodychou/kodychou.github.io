<!DOCTYPE html>
<html lang="{{ site.lang | default: 'en' | escape }}">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>{{ site.title | escape }}</title>
<meta name="description" content="{{ site.description | escape }}">
<meta name="theme-color" content="#137568">
<style>
/* Edit colors here. All styling stays in this file so only two files are needed. */
:root { --bg: #f6f7f4; --paper: #fff; --ink: #182b29; --muted: #526561; --accent: #137568; --line: #dce4df; --soft: #eaf3ed; }
* { box-sizing: border-box; }
html { scroll-behavior: smooth; scroll-padding-top: 24px; }
body { margin: 0; background: var(--bg); color: var(--ink); font: 16px/1.7 system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif; }
a { color: var(--accent); text-underline-offset: 4px; }
a:hover { text-decoration-thickness: 2px; }
a:focus-visible { outline: 3px solid var(--accent); outline-offset: 5px; border-radius: 3px; }
.wrap { max-width: 1160px; margin: 0 auto; padding: 0 40px; }
.skip { position: absolute; left: 20px; top: -100px; background: var(--paper); padding: 12px 20px; z-index: 5; }
.skip:focus { top: 12px; }
.topbar { display: flex; align-items: center; justify-content: space-between; gap: 24px; padding: 27px 0; border-bottom: 1px solid var(--line); }
.brand { display: flex; align-items: center; gap: 12px; color: var(--ink); font-weight: 700; text-decoration: none; }
.monogram { display: grid; place-items: center; width: 40px; height: 40px; border-radius: 12px; color: white; background: var(--accent); font-size: 14px; letter-spacing: .04em; }
nav { display: flex; flex-wrap: wrap; gap: 25px; }
nav a { color: var(--muted); text-decoration: none; font-size: 14px; font-weight: 600; }
nav a:hover { color: var(--accent); }
.hero { padding: 66px 0 55px; max-width: 870px; }
.eyebrow { margin: 0 0 15px; color: var(--accent); font-size: 12px; font-weight: 750; text-transform: uppercase; letter-spacing: .14em; }
h1 { font-size: clamp(36px, 4.8vw, 58px); line-height: 1.12; letter-spacing: -.045em; margin: 0 0 20px; max-width: 820px; }
.role { font-size: 15px; color: var(--muted); margin: 0 0 20px; }
.about { max-width: 755px; color: var(--muted); font-size: 17px; margin: 0 0 26px; }
.actions { display: flex; flex-wrap: wrap; align-items: center; gap: 12px; }
.button { display: inline-flex; align-items: center; justify-content: center; min-height: 44px; padding: 9px 18px; border: 1px solid var(--line); border-radius: 8px; color: var(--ink); background: var(--paper); font-size: 14px; font-weight: 650; text-decoration: none; }
.button.primary { color: white; background: var(--accent); border-color: var(--accent); }
.button:hover { box-shadow: 0 3px 10px #182b2910; text-decoration: underline; }
.content { display: grid; grid-template-columns: minmax(0, 1fr) 294px; align-items: start; gap: 34px; padding-bottom: 66px; }
.section-heading { display: flex; align-items: baseline; justify-content: space-between; gap: 15px; margin-bottom: 20px; }
h2 { margin: 0; font-size: 23px; line-height: 1.3; letter-spacing: -.025em; }
.count { color: var(--muted); font-size: 12px; letter-spacing: .08em; text-transform: uppercase; }
.project { margin-bottom: 18px; padding: 27px 29px; background: var(--paper); border: 1px solid var(--line); border-radius: 14px; }
.project:last-child { margin-bottom: 0; }
.project .eyebrow { font-size: 10px; margin-bottom: 9px; }
h3 { font-size: 23px; line-height: 1.3; letter-spacing: -.025em; margin: 0 0 12px; }
.project p.description { margin: 0 0 17px; color: var(--muted); font-size: 15px; }
.tags { display: flex; flex-wrap: wrap; gap: 7px; list-style: none; padding: 0; margin: 0 0 20px; }
.tags li { background: var(--soft); border-radius: 5px; padding: 3px 9px; color: #34574c; font-size: 11px; font-weight: 600; }
.project-links { display: flex; flex-wrap: wrap; gap: 12px 23px; }
.project-links a { font-weight: 650; font-size: 13px; }
.sidebar { margin-top: 50px; background: var(--paper); border: 1px solid var(--line); border-radius: 14px; padding: 26px 23px; }
.sidebar h2 { font-size: 20px; }
.sidebar-intro { font-size: 12px; color: var(--muted); margin: 10px 0 18px; }
.language-list { margin: 0; }
.language { display: flex; justify-content: space-between; gap: 12px; align-items: baseline; padding: 11px 0; border-bottom: 1px solid var(--line); }
.language:last-child { border-bottom: 0; }
.language dt { font-size: 13px; font-weight: 650; }
.language dd { margin: 0; text-align: right; font-size: 11px; color: var(--muted); }
.sidebar-section { margin-top: 25px; padding-top: 22px; border-top: 1px solid var(--line); }
.sidebar-section h3 { font-size: 13px; letter-spacing: 0; margin: 0 0 13px; }
.sidebar .tags { gap: 6px; margin: 0; }
.sidebar .tags li { font-size: 11px; background: var(--bg); color: var(--muted); }
footer { border-top: 1px solid var(--line); padding: 25px 0; display: flex; justify-content: space-between; flex-wrap: wrap; gap: 12px; color: var(--muted); font-size: 12px; }
footer p { margin: 0; }
@media (max-width: 800px) {
  .wrap { padding: 0 24px; }
  .content { grid-template-columns: minmax(0, 1fr); gap: 30px; }
  .sidebar { margin-top: 0; }
  .hero { padding: 47px 0 40px; }
}
@media (max-width: 480px) {
  .wrap { padding: 0 18px; }
  .topbar { flex-direction: column; align-items: flex-start; gap: 16px; padding: 21px 0; }
  nav { gap: 22px; }
  .project { padding: 24px 21px; }
  .section-heading { align-items: center; }
  .count { font-size: 10px; }
}
@media (prefers-reduced-motion: reduce) { html { scroll-behavior: auto; } }
</style>
</head>
<body>
<a class="skip" href="#main">Skip to content</a>
<div class="wrap">
  <header class="topbar">
    <a class="brand" href="#about">
      <span class="monogram" aria-hidden="true">{{ site.profile.initials | escape }}</span>
      {{ site.profile.name | escape }}
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
      <h1 id="about-heading">{{ site.profile.introduction | escape }}</h1>
      <p class="role">{{ site.profile.role | escape }}</p>
      <p class="about">{{ site.profile.about | escape }}</p>
      <div class="actions">
        <a class="button primary" href="#projects">Explore my work <span aria-hidden="true">&nbsp;↘</span></a>
        <a class="button" href="mailto:{{ site.profile.email | escape }}">Get in touch</a>
        {% if site.profile.github_url != blank %}
        <a class="button" href="{{ site.profile.github_url | escape }}">GitHub <span aria-hidden="true">&nbsp;↗</span></a>
        {% endif %}
        {% if site.profile.linkedin_url != blank %}
        <a class="button" href="{{ site.profile.linkedin_url | escape }}">LinkedIn <span aria-hidden="true">&nbsp;↗</span></a>
        {% endif %}
      </div>
    </section>
    <div class="content">
      <section id="projects" aria-labelledby="projects-heading">
        <div class="section-heading">
          <h2 id="projects-heading">Selected projects</h2>
          <span class="count">{{ site.projects | size }} projects</span>
        </div>
        {% for project in site.projects %}
        <article class="project" aria-labelledby="project-{{ forloop.index }}">
          <p class="eyebrow">{{ project.category | escape }}</p>
          <h3 id="project-{{ forloop.index }}">{{ project.name | escape }}</h3>
          <p class="description">{{ project.description | escape }}</p>
          {% if project.technologies.size > 0 %}
          <ul class="tags" aria-label="Technologies and focus areas">
            {% for technology in project.technologies %}
            <li>{{ technology | escape }}</li>
            {% endfor %}
          </ul>
          {% endif %}
          <div class="project-links">
            {% if project.demo_url != blank %}
            <a href="{{ project.demo_url | escape }}" aria-label="{{ project.demo_label | default: 'View project' | escape }}: {{ project.name | escape }}">{{ project.demo_label | default: 'View project' | escape }} <span aria-hidden="true">↗</span></a>
            {% endif %}
            {% if project.source_url != blank %}
            <a href="{{ project.source_url | escape }}" aria-label="View source code for {{ project.name | escape }}">Source code <span aria-hidden="true">↗</span></a>
            {% endif %}
            {% if project.demo_url == blank and project.source_url == blank %}
            <a href="mailto:{{ site.profile.email | escape }}?subject={{ project.name | url_encode }}" aria-label="Ask about {{ project.name | escape }}">Ask about this project <span aria-hidden="true">↗</span></a>
            {% endif %}
          </div>
        </article>
        {% endfor %}
      </section>
      <aside id="languages" class="sidebar" aria-labelledby="languages-heading">
        <h2 id="languages-heading">Languages</h2>
        <p class="sidebar-intro">My experience at a glance.</p>
        <dl class="language-list">
          {% for language in site.languages %}
          <div class="language">
            <dt>{{ language.name | escape }}</dt>
            <dd>{{ language.level | escape }}</dd>
          </div>
          {% endfor %}
        </dl>
        <section class="sidebar-section" aria-labelledby="web-heading">
          <h3 id="web-heading">Web technologies</h3>
          <ul class="tags">
            {% for technology in site.web_technologies %}
            <li>{{ technology | escape }}</li>
            {% endfor %}
          </ul>
        </section>
        <section class="sidebar-section" aria-labelledby="tools-heading">
          <h3 id="tools-heading">Tools &amp; platforms</h3>
          <ul class="tags">
            {% for tool in site.tools %}
            <li>{{ tool | escape }}</li>
            {% endfor %}
          </ul>
        </section>
      </aside>
    </div>
  </main>
  <footer>
    <p>© {{ 'now' | date: '%Y' }} {{ site.profile.name | escape }}</p>
    <a href="mailto:{{ site.profile.email | escape }}">Let's connect <span aria-hidden="true">↗</span></a>
  </footer>
</div>
</body>
</html>
