---
title: "Data Simulation & Basis Set Generation"
permalink: /software_simulation/
date: 2020-05-15T9:00:00+00:00
sidebar:
  nav: "software"
toc: true
---
This is a list of simulation software.

{% for software_collection in site.software_collection %}
  {% if software_collection.type contains "simulation" %}
  <h2>
      {{ software_collection.name }}
  </h2>
  <img src= "{{ site.url }}{{ site.baseurl }}{{ software_collection.image }}" alt="" align="right"/>
  <p>{{ software_collection.abstract | markdownify }}</p>
  Developer: {{ software_collection.developer }} <br>
  Language: {{ software_collection.language }} <br>
  License: {{ software_collection.license }} <br>
  Credit: {{ software_collection.credit }} <br>
  {% if software_collection.mrshub_url %}<a href="{{ software_collection.mrshub_url }}">MRSHub Code</a>&nbsp;{% endif %}
  {% if software_collection.original_url %}<a href="{{ software_collection.original_url }}">Original Website</a>&nbsp;{% endif %}
  {% if software_collection.paper %}<a href="{{ software_collection.paper }}">Publication</a>{% endif %}
  {% endif %}
{% endfor %}
