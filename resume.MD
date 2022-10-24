---
layout: page
title: Resume
permalink: /resume/
---

<br>This is where I will put my full resume when I feel like it.<br>

{% for job in site.data.resume %}
<div>
    <h1>{{ job.title }}</h1>
    <strong>{{ job.employer }}</strong> {{ job.startdate }} - {{ job.enddate }} <br>
    {% for skill in job.skills %}
        | {{ skill }}
    {% endfor %} |
    <br>
    <ul>
    {% for item in job.description %}
    <li>{{ item }}</li>
    {% endfor %}
    </ul>
</div><br>
{% endfor %}

