---
layout: default
title: Βιογραφικό - Φαίδων Τσέτσης
lang: el
---

# {{ site.data.resume-el.name }}
### {{ site.data.resume-el.title }}

{{ site.data.resume-el.about_content }}

{% for section in site.data.resume-el.content %}
  <div class="container {{ section.layout }}-container">
    <h3>{{ section.title }}</h3>
    {% for item in section.content %}
      <div>
        <strong>{{ item.title }}</strong>
        <em>{{ item.sub_title }}</em>
        {% if item.description %}
          <ul>
            {% for desc in item.description %}
              <li>{{ desc }}</li>
            {% endfor %}
          </ul>
        {% endif %}
      </div>
    {% endfor %}
  </div>
{% endfor %}
