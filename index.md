---
title: Online Hosted Instructions
permalink: index.html
layout: home
---

# Deconstructing Contoso Real Estate

Links to the Glossary, Lab Exercises and Demo Videos used for Learn Labs on exploring [Contoso Real Estate](https://aka.ms/contoso-real-estate/github)

## Glossary

{% assign glossary = site.pages | where_exp:"page", "page.url contains '/Glossary'" %}

| Type | Resource |
| --- | --- | 
{% for activity in glossary  %} | {{ activity.type.description }} | [{{ activity.type.title }}]({{ site.github.url }}{{ activity.url }}) |
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
