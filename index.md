---
title: Online Hosted Instructions
permalink: index.html
layout: home
---

# Deconstructing Contoso Real Estate

Resources to help self-guided exploration of the [Contoso Real Estate](https://aka.ms/contoso-real-estate/github) reference architecture and samples.


## Lab Exercises

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Labs'" %}
| Module | Lab |
| --- | --- | 
{% for activity in labs  %} | {{ activity.lab.module }} | [{{ activity.lab.title }}{% if activity.lab.type %} - {{ activity.lab.type }}{% endif %}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## Demo Videos

{% assign demos = site.pages | where_exp:"page", "page.url contains '/Instructions/Demos'" %}
| Module | Demo Video |
| --- | --- | 
{% for activity in demos  %}| {{ activity.demo.module }} | [{{ activity.demo.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## Live Sessions

{% assign live = site.pages | where_exp:"page", "page.url contains '/Instructions/Live'" %}
| Session | Description | Date |
| --- | --- | ---|
{% for activity in live  %} | {{ activity.session.title }} | [{{ activity.session.date }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

## Glossary

{% assign glossary = site.pages | where_exp:"page", "page.url contains '/Glossary'" %}
| Description | Section |
| --- | --- | 
{% for activity in glossary  %} | {{ activity.section.description }} | [{{ activity.section.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}