---
layout: default
permalink: /
---

<link rel="shortcut icon" type="image/x-icon" href="{{ "/images/favicon.ico" | prepend: site.baseurl }}" >

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

</style>

<audio id="ping" src="/sounds/26.mp3"></audio>

<h1 class="page-title">Click for a surprise</h1>

<div id="visitor-counter">Loading visitor count...</div>

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
document.addEventListener("DOMContentLoaded", function() {
    const apiKey = '046fec97b651917ca87605b1c98002bba3859f91';
    const apiUrl = 'https://api.cptmilk.xyz/visit?api_key=' + apiKey;

    // POST request increments the visitor count
    fetch(apiUrl, { method: 'POST' })
      .then(() => {
        return fetch(apiUrl, { method: 'GET' });
      })
      .then(response => response.json())
      .then(data => {
        document.getElementById('visitor-counter').textContent = 'Visitor Count: ' + data.visitor_count;
      })
      .catch(error => {
        console.error('Error fetching visitor count:', error);
        document.getElementById('visitor-counter').textContent = 'Error loading visitor count.';
      });

    var attribution = document.getElementById("attribution");
    if (attribution) {
        attribution.style.display = "none";
    }
});  
</script>
