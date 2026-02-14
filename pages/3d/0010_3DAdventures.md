---
layout: default
title:  3D Creations
type: other
nav_name: 3D Creations
---

<div class="centered highlighted_top larger_text">
<h1>My 3D Creations</h1>
<p>
    I like to play around with different tools from time to time. I am interested in 3D graphics, compositing scenes and would like to improve my 3D modeling skills. This page should act as a gallery for any future endeavors into these kinds of topics. 
</p>
<p>
    When focusing on composition, I tend to use freely available assets and therefore must give proper <a href="0000_credits.html">credit</a>.
</p>
</div>

<div class="centered">
<h2>Gallery</h2>

{% assign images = site.static_files
  | where_exp: "file", "file.path contains '/assets/3dgallery/'" %}

<div  class="gallery">
{% for img in images %}
  {% if img.extname == ".png" %}
<img src="../../{{ img.path }}" class="grow-image" tabindex="0">
  {% endif %}
{% endfor %}
<div>

</div>