---
layout: page
title: About
permalink: /about/
weight: 3
---

<link rel="shortcut icon" type="image/x-icon" href="{{ "/images/favicon.ico" | prepend: site.baseurl }}" >

# **About Me**

Hello! I am fraudwrd, or fraud for short,<br>
I have been on the internet for some time now, and it has been an exceptional experience! During my time online however, I have learned a variety of skills that may be of interest to anyone reading this wanting to hire me for their studio.<br>
I love doing management related duties and managing groups, but handling all the boring paperwork is a fun pastime to me!<br>
I also pride myself in my moderation skills. I, as passionate as I am about law enforcement, maintain a non-bias, compassionate standpoint when it comes to moderation.<br>
I can also brew up some pretty nice liveries! I normally don't do this outside of my own servers, but as long as the request comes with compensation I'll consider it. You can find some of my livery work in the "My work" portion of this website.<br>
Finally, if you've made it to here, I like to see myself as an experienced vehicle tuner who primarily works with A-Chassis and is constantly working to make vehicles feel as realistic as possible within Roblox!

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
