---
layout: current_project
title:  A year of Backgrounds
type: current_project
nav_name: The 52 Backgrounds

project_name: A year of Backgrounds
project_description: |
    A project of forcing myself to create some sort of "background art" for every week of the year. The idea came with the need to replace the default one on a new PC. After experimenting with some drawing methods I decided to commit to a whole year of experimentation.
---

Initially I wrote a basic C# program which could load a specified Assembly, from which a painter type could be selected to draw into an image of a specified size. The Assembly contains the actual definition for the painters. I chose this kind of architecture to practice working with reflection in C#, but also it's more loosely coupled this way.

The formal-ish self-imposed requirements for each creation are:
- a piece of code that can generate infinitely many similar images
- the generated images must cover at least a two-monitor setup
- the images should loop on all sides seamlessly

All of these are more like guidelines and might be broken.


Eventually I wanted more control in my creative process and faster iteration. I created a GUI application which can load the Assembly in much the same fashion. Since this loading is dynamic, the Assembly can be rebuilt and reloaded all on runtime. The application also allows for manual variable manipulation via controls like sliders or number entries, which can directly affect the drawing process. Below is a snippet from the current version of the app.

<img src="painter.png" style="width:80%; margin: auto; display: flow;">

The application is WIP, I might provide a link to the source code at some point in the future.

---

# Gallery

{% assign images = site.static_files
  | where_exp: "file", "file.path contains '/assets/52backs/'" %}

<div  class="gallery">
{% for img in images %}
  {% if img.extname == ".png" %}
<img src="../../{{ img.path }}" class="grow-image" tabindex="0">
  {% endif %}
{% endfor %}
<div>