---
layout: default
permalink: /
---

<link rel="shortcut icon" type="image/x-icon" href="{{ "/images/favicon.ico" | prepend: site.baseurl }}" >

{% include landing.html %}
 
<button>
    P L A Y
    <div id="clip">
        <div id="leftTop" class="corner"></div>
        <div id="rightBottom" class="corner"></div>
        <div id="rightTop" class="corner"></div>
        <div id="leftBottom" class="corner"></div>
    </div>
    <span id="rightArrow" class="arrow"></span>
    <span id="leftArrow" class="arrow"></span>
</button>

<script>
 document.querySelector('.page-title').addEventListener('click', function() {
    var audio = document.getElementById("ping");
    audio.play();
  });

document.addEventListener("DOMContentLoaded", function() {
    var attribution = document.getElementById("attribution");
    if (attribution) {
        attribution.style.display = "none";
    }
});    
</script>
