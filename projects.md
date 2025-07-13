---
layout: page-wide
title: Projects
emoji: 🏗️
permalink: /projects
---

{% include project_filters.html %}

## Current
Main projects I am currently working on.

<section class="projects">
    {% assign current_projects = site.projects | where: "current", true | sort: "publish_date", "last" | reverse %}
    {% for project in current_projects %}
        {% include project_card.html %}
    {% endfor %}
</section>

## Past
Projects I have worked on in the past but have put on hold or don't intend to update further.

<section class="projects">
    {% assign sorted_projects = site.projects | where: "current", false | sort: "publish_date", "last" | reverse %}
    {% for project in sorted_projects %}
        {% include project_card.html %}
    {% endfor %}
</section>
