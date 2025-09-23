---
layout: page
title: Outcomes
permalink: /publications/
feature-img: "assets/img/pexels/book-glass.jpeg"
excluded: true
position: 4
tags: [Page]
---

<!-- Project Reports Section -->
<div class="category-section">
  <h2 class="category-title">📊 Project Reports</h2>
  <div class="category-description">
    <p>Comprehensive reports documenting project outcomes, methodologies, and findings.</p>
  </div>
  
  {% assign report_count = 1 %}
  {% assign has_reports = false %}
  {% for post in site.posts %}
    {% if post.categories contains "Publications" and post.subcategory == "Project Reports" %}
      {% assign has_reports = true %}
      <div class="publication report" style="border-left: 4px solid #e74c3c; padding: 15px; margin-bottom: 15px; background-color: #fdf2f2; border-radius: 5px;">
        <h3 class="publication-title">{{ report_count }}. <a href="{{ post.url }}" style="color: #c0392b; text-decoration: none;">{{ post.title }}</a></h3>
        {% if post.excerpt %}
          <p class="publication-excerpt" style="color: #7f8c8d; font-size: 0.9em; margin-top: 8px;">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
        {% endif %}
        {% if post.date %}
          <span class="publication-date" style="color: #95a5a6; font-size: 0.8em;">{{ post.date | date: "%B %Y" }}</span>
        {% endif %}
      </div>
      {% assign report_count = report_count | plus: 1 %}
    {% endif %}
  {% endfor %}
  
  {% unless has_reports %}
    <p class="no-content" style="color: #7f8c8d; font-style: italic;">No project reports available yet.</p>
  {% endunless %}
</div>

<!-- Scientific Articles Section -->
<div class="category-section" style="margin-top: 40px;">
  <h2 class="category-title">📝 Scientific Articles</h2>
  <div class="category-description">
    <p>Peer-reviewed publications and research articles in academic journals and conferences.</p>
  </div>
  
  {% assign article_count = 1 %}
  {% assign has_articles = false %}
  {% for post in site.posts %}
    {% if post.categories contains "Publications" and post.subcategory == "Scientific Articles" %}
      {% assign has_articles = true %}
      <div class="publication article" style="border-left: 4px solid #3498db; padding: 15px; margin-bottom: 15px; background-color: #f8fbfc; border-radius: 5px;">
        <h3 class="publication-title">{{ article_count }}. <a href="{{ post.url }}" style="color: #2980b9; text-decoration: none;">{{ post.title }}</a></h3>
        {% if post.article_title %}
          <p class="article-title" style="color: #2c3e50; font-weight: 600; margin-top: 8px; font-size: 1.05em;">"{{ post.article_title }}"</p>
        {% endif %}
        {% if post.journal %}
          <p class="publication-journal" style="color: #34495e; font-weight: 500; margin-top: 5px;"><em>{{ post.journal }}</em></p>
        {% endif %}
        {% if post.excerpt %}
          <p class="publication-excerpt" style="color: #7f8c8d; font-size: 0.9em; margin-top: 8px;">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
        {% endif %}
        {% if post.date %}
          <span class="publication-date" style="color: #95a5a6; font-size: 0.8em;">{{ post.date | date: "%B %Y" }}</span>
        {% endif %}
      </div>
      {% assign article_count = article_count | plus: 1 %}
    {% endif %}
  {% endfor %}
  
  {% unless has_articles %}
    <p class="no-content" style="color: #7f8c8d; font-style: italic;">No scientific articles available yet.</p>
  {% endunless %}
</div>

<!-- Source Code Section -->
<div class="category-section" style="margin-top: 40px;">
  <h2 class="category-title">💻 Source Code</h2>
  <div class="category-description">
    <p>Open-source code repositories, software tools, and technical implementations.</p>
  </div>
  
  {% assign code_count = 1 %}
  {% assign has_code = false %}
  {% for post in site.posts %}
    {% if post.categories contains "Publications" and post.subcategory == "Source Code" %}
      {% assign has_code = true %}
      <div class="publication code" style="border-left: 4px solid #27ae60; padding: 15px; margin-bottom: 15px; background-color: #f8fffe; border-radius: 5px;">
        <h3 class="publication-title">{{ code_count }}. <a href="{{ post.url }}" style="color: #229954; text-decoration: none;">{{ post.title }}</a></h3>
        {% if post.github_url %}
          <p class="publication-github" style="margin-top: 5px;">
            <a href="{{ post.github_url }}" style="color: #2ecc71; text-decoration: none; font-size: 0.9em;">
              🔗 View on GitHub
            </a>
          </p>
        {% endif %}
        {% if post.programming_language %}
          <span class="programming-language" style="background-color: #d5f4e6; color: #27ae60; padding: 2px 8px; border-radius: 12px; font-size: 0.8em; margin-top: 8px; display: inline-block;">{{ post.programming_language }}</span>
        {% endif %}
        {% if post.excerpt %}
          <p class="publication-excerpt" style="color: #7f8c8d; font-size: 0.9em; margin-top: 8px;">{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
        {% endif %}
        {% if post.date %}
          <span class="publication-date" style="color: #95a5a6; font-size: 0.8em;">{{ post.date | date: "%B %Y" }}</span>
        {% endif %}
      </div>
      {% assign code_count = code_count | plus: 1 %}
    {% endif %}
  {% endfor %}
  
  {% unless has_code %}
    <p class="no-content" style="color: #7f8c8d; font-style: italic;">No source code repositories available yet.</p>
  {% endunless %}
</div>

<style>
.category-title {
  color: #2c3e50;
  border-bottom: 2px solid #ecf0f1;
  padding-bottom: 10px;
  margin-bottom: 20px;
}

.category-description {
  margin-bottom: 25px;
  color: #5d6d7e;
}

.publication-title a:hover {
  text-decoration: underline !important;
}

.publication {
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.publication:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}
</style>