---
layout: page
title: Resume
permalink: /resume/
---

<br>This is where I will put my full resume when I feel like it.<br>

{% for job in site.data.resume %}
<div>
    <h1 style="text-align:center;">{{ job.title }}</h1>
    {{ job.employer }}<br>
    <small>{{ job.startdate }} - {{ job.enddate }}</small><br>
    Skills:<br>
    {% for skill in job.skills %}
        {% if skill != job.skills.first -%}
            |
        {% endif %} 
        {{ skill }}
    {% endfor %}
    <br>
    <ul>
    {% for item in job.description %}
    {% if item.first %}
        <ul><ul>
        {% for subitem in item %}
            <li>{{ subitem }}</li>
        {% endfor %}
        </ul></ul>
    {% else %}
        <li>{{ item }}</li>
    {% endif %}
    {% endfor %}
    </ul>
    {% endfor %}
</div><br>