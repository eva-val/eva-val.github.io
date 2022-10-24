---
layout: page
title: Job Transparency
permalink: /job-transparency/
---

<br>This is my job and salary transparency. It's kept seperate from the resume as it is my full job history will salary. I also don't give recruiter friendly reasons why I left =)
Inspired by [Xe's page][xe-jobs] on giving full transparency.
<style>
    table, th, td {
        border: 1px solid white;
        border-style: dashed;
        border-collapse: collapse;
    }
</style>
<table>
    <tr>
        <th>Job Title</th>
        <th>Job Type</th>
        <th>Start Date</th>
        <th>End Date</th>
        <th>Salary</th>
        <th>How I Left</th>
        <th>Why I Left</th>
    </tr>
    {% for item in site.data.jobs %}
    <tr>
        <td>{{ item.title }}</td>
        <td>{{ item.type }}</td>
        <td>{{ item.startdate }}</td>
        <td>{{ item.enddate }}</td>
        <td>{{ item.salary }}</td>
        <td>{{ item.howileft }}</td>
        <td>{{ item.whyileft }}</td>
    </tr>
    {% endfor %}
</table>

[xe-jobs]: https://xeiaso.net/salary-transparency