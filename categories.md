---
layout: page
title: Skills
permalink: /categories/
---




{% for category in site.categories %}
<div class="catbloc" id="{{ category | first | remove:' ' }}">
          <h2>{{ category | first }}</h2>      
          <ul>
             {% for posts in category %}
               {% for post in posts %}
                 {% if post.url %}
                   <li>
                    <a href="{{ post.url }}">
                      <time>{{ post.date | date: "%Y-%m-%d" }}</time> &raquo;
                      {{ post.title }}
                    </a>
                  </li>
                {% endif %}
               {% endfor %}
            {% endfor %}
         </ul>
     </div>
{% endfor %}