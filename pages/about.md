---
layout: page
title: About
permalink: /about/
weight: 3
---

<link rel="shortcut icon" type="image/x-icon" href="{{ "/images/favicon.ico" | prepend: site.baseurl }}" >

# **About Me**

Hello! I am fraudwrd, or fraud for short :wave:,<br>
I have been on the internet for some time now, and it has been an exceptional experience! During my time online however, I have learned a variety of skills that may be of interest to anyone reading this wanting to hire me for their studio. I love doing management related duties, managing groups and handling all the boring paperwork is a fun pastime to me! I also pride myself in my moderation skills. I, as passionate as I am about law enforcement, maintain a non-bias, compassionate standpoint when it comes to moderation. I can also brew up some pretty nice liveries! I normally don't do this outside of my own servers, but as long as the request comes with compensation I'll consider it. You can find some of my livery work in the Projects portion of this website. Finally, if you've made it to here, I like to see myself as an amateur programmer in Luau. I mainly focus on quality-of-life features for experiences on Roblox.

<div class="row">
{% include about/skills.html title="Skills" source=site.data.other-skills %}
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
