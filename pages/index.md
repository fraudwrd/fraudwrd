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
</script>

<script>
  // Replace with your actual API endpoint and API key
  const apiKey = 'e72e59c858c24149a8aa0cd3e442a110841bf6b8';
  const apiUrl = 'https://api.cptmilk.xyz/visit?api_key=' + apiKey;

  // Fetch the current visitor count (does not increment)
  fetch(apiUrl)
    .then(response => response.json())
    .then(data => {
      document.getElementById('visitor-counter').textContent = 
        'Visitor Count: ' + data.visitor_count;
    })
    .catch(error => {
      console.error('Error fetching visitor count:', error);
      document.getElementById('visitor-counter').textContent = 'Error loading visitor count.';
    });
</script>

<script>
  // This code will send a POST request to increment the visitor count.
  fetch('https://api.cptmilk.xyz/visit?api_key=' + apiKey, {
    method: 'POST'
  })
    .then(response => response.json())
    .then(data => {
      console.log('Updated visitor count:', data.visitor_count);
      // Optionally update the counter on your page here
    })
    .catch(error => console.error('Error incrementing count:', error));
</script>
