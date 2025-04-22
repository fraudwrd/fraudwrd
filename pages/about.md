---
layout: page
title: About
permalink: /about/
weight: 3
---

<link rel="shortcut icon" type="image/x-icon" href="{{ "/assets/favicon.ico" | prepend: site.baseurl }}" >

# **About Me**

Hello! I am fraudwrd, or fraud for short. I have been on the internet for some time now, and it has been an exceptional experience! During my time online however, I have learned a variety of skills that may be of interest to anyone reading this wanting to hire me for their studio. Below, you can find what I am most skilled at, and you can find some of my work displaying these skills in the 'My Work' portion of my website.

<div class="row">
{% include about/skills.html title="Management Skills" source=site.data.other-skills %}
{% include about/skills.html title="Design Skills" source=site.data.programming-skills %}
</div>

<div class="row">
{% include about/timeline.html %}
</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
    var attribution = document.getElementById("attribution");
    if (attribution) {
        attribution.style.display = "none";
    }
});    
</script>
