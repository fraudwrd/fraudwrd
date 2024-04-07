---
layout: default
permalink: /
---

<link rel="shortcut icon" type="images/x-icon" href="{{ "/images/favicon.ico" | prepend: site.baseurl }}" >

{% include landing.html %}

<style>
@keyframes rainbow {
  0% { color: red; }
  20% { color: orange; }
  40% { color: yellow; }
  60% { color: green; }
  80% { color: blue; }
  100% { color: violet; }
}

.page-title {
  animation: rainbow 5s infinite; /* Change 5s to adjust speed */
  text-align: center; /* Center the text */
  cursor: pointer; /* Change cursor on hover */
}

.scroll-text {
  text-align: center
  overflow: hidden;
  white-space: nowrap;
}

.scroll-text .rainbow-text {
  display: inline-block;
  animation: scroll 10s linear infinite; /* Change 10s to adjust speed */
}

@keyframes scroll {
  0% { transform: translateX(100%); }
  100% { transform: translateX(-100%); }
}
</style>

<audio id="ping" src="/sounds/3.mp3"></audio>

<h1 class="page-title">Click for a surprise</h1>

<div class="scroll-text">
  <span class="rainbow-text">BREAKING NEWS: FRAUD IS A FRAUD | BREAKING NEWS: FRAUD IS A FRAUD | BREAKING NEWS: FRAUD IS A FRAUD</span>
</div>

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
