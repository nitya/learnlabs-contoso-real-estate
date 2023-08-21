---
title: Online Hosted Instructions
permalink: index.html
layout: home
---

# Deconstructing Contoso Real Estate

Resources to help self-guided exploration of the [Contoso Real Estate](https://aka.ms/contoso-real-estate/github) reference architecture and samples.

## Glossary

The Contoso Real Estate Application may use terms, tools and technologies that are new to you. Check out these Glossary sections to get a brief description of each along with a link for deep dives.

{% assign glossary = site.pages | where_exp:"page", "page.url contains '/Glossary'" %}
{% for activity in glossary  %} - [{{ activity.type.title }}]({{ site.github.url }}{{ activity.url }}) 
{% endfor %}

## Learn Live Sessions

Want some instructor guidance into the exercises before you dive in solo? We have you covered! Check out these Learn Live sessions (planned for Sep/Oct 2023) and bookmark the page to revisit recordings later.

{% assign live = site.pages | where_exp:"page", "page.url contains '/Instructions/Live'" %}
| Description | Session |
| --- | --- | 
{% for activity in live  %} | {{ activity.session.title }} | [{{ activity.session.date }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}

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
