---
layout: custom-projects
title: Welcome to my page!
show_collection: projects
cover: true
---

<div class="welcome-section" style="text-align: left !important;">

I am a Data Passionate with expertise in building end-to-end data solutions, from ETL pipelines to interactive visualizations and predictive Machine Learning models. With a background in <b>Computer Science</b> and <b>Data Analytics Engineering</b>, I combine technical expertise with analytical problem-solving.


<div style="margin-top: 30px;"></div>
<div class="expertise-highlights" style="text-align: left !important;">
  <p><b>Explore Pages:</b></p>
  <ul>
    <a href="https://yannacs.github.io/about/" onclick="event.stopPropagation();">About Me</a> Learn more about my skills, expertise, and interests.
    <br>
	  <a href="https://yannacs.github.io/projects/" onclick="event.stopPropagation();">Projects</a> Discover detailed examples of my work and accomplishments.
  </ul>
</div>

<div class="contact-section" style="margin-top: 20px;">
  <p><b>More:</b></p>
  <div class="social-icons">
    {% comment %}Get the author's social links{% endcomment %}
    {% assign author = site.data.authors[page.author] | default: site.data.authors.first[1] | default: site.author %}
    
    {% if author.social %}
      {% for social in author.social %}
        {% assign platform = social[0] %}
        {% assign username = social[1] %}
        {% assign social_info = site.data.social[platform] %}
        
        {% if social_info and username %}
          {% comment %}Build the full URL{% endcomment %}
          {% assign url = "" %}
          {% if platform == "email" %}
            {% assign url = "mailto:" | append: username %}
          {% else %}
            {% assign url = social_info.prepend | append: username | append: social_info.append %}
          {% endif %}
          
          <a href="{{ url }}" class="social-link" 
             {% unless platform == "email" %}target="_blank" rel="noopener"{% endunless %}>
            <i class="{{ social_info.icon }}"></i> {{ social_info.name }} 
          </a><br>
        {% endif %}
      {% endfor %}
    {% endif %}
  </div>
</div>

<!--
<div class="hint">
  <span class="hint-icon">💡</span>
  <span class="hint-text">Please use the sidebar to connect with me and access my latest resume.</span>
</div>
<div style="margin-bottom: 30px;"></div>
<div class="expertise-highlights" style="text-align: left !important;">
  <p><b>I specialize in:</b></p>
  <ul>
    <li>Creating normalized database schemas and optimizing data models</li>
    <li>Developing interactive dashboards that transform data into actionable insights</li>
    <li>Building predictive models using scikit-learn, TensorFlow and statistical methods</li>
    <li>Implementing ETL pipelines for efficient data processing and integration</li>
  </ul>
</div>

<div style="margin-bottom: 30px;"></div>
<div class="projects-intro" style="text-align: left !important;">
  <p><b>Browse my projects showcasing skills in:</b></p>
  <ul class="skill-tags">
    <li>Data Engineering & ETL</li>
    <li>Machine Learning</li>
    <li>Data Visualization</li>
    <li>Database Design</li>
    <li>NLP & Computer Vision</li>
  </ul>
</div>
-->

</div>