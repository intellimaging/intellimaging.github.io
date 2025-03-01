---
title: "Intellimaging Tech - Home"
layout: homelay
excerpt: "Developing artificial intelligence technologies for medical imaging"
sitemap: false
permalink: /
---
<html>    
<body>
<p style="text-align: justify;">Artificial Intelligence (AI) is revolutionizing medical imaging by enhancing diagnostic precision, streamlining workflow efficiency, and enabling early disease detection. Leveraging machine learning (ML) and deep learning (DL) techniques, AI-driven tools interpret complex medical images—such as MRIs, CT scans, and ultrasounds—transforming radiology and extending its reach across healthcare. These tools expertly identify abnormalities like tumors, fractures, and infections, while supporting early detection of cancers, cardiovascular diseases, and neurological disorders. AI accurately delineates anatomical structures and lesions, facilitating surgical planning, radiation therapy, and other interventions. Additionally, it distinguishes benign from malignant lesions, categorizes disease subtypes, informs personalized treatment strategies, and measures tumor volume, organ size, and vascular characteristics while tracking disease progression and treatment response. Specializing in X-ray tomographic imaging, photoacoustic imaging, and advanced image reconstruction and analysis, we are developing innovative theories, methods, software, and hardware systems for clinical use in disease detection and diagnosis. We welcome collaboration with partners and funding agencies on transformative, high-impact projects.</p>

<div class="w3-content w3-display-container">
  <img class="mySlides" src="{{ site.url }}{{ site.baseurl }}/images/Slide1.PNG" style="width:100%">
  <img class="mySlides" src="{{ site.url }}{{ site.baseurl }}/images/Slide000.png" style="width:100%">
  <img class="mySlides" src="{{ site.url }}{{ site.baseurl }}/images/Slide11.png" style="width:100%">
  <img class="mySlides" src="{{ site.url }}{{ site.baseurl }}/images/Slide3.png" style="width:100%">
</div>
<div style="text-align: center;">
  <button class="w3-button w3-black w3-display-left" onclick="plusDivs(-1)">❮ Prev</button>
  <button class="w3-button w3-black w3-display-right" onclick="plusDivs(1)">Next ❯</button>
</div>

<script>
var slideIndex = 1;
showDivs(slideIndex);

function plusDivs(n) {
  showDivs(slideIndex += n);
}

function showDivs(n) {
  var i;
  var x = document.getElementsByClassName("mySlides");
  if (n > x.length) {slideIndex = 1}
  if (n < 1) {slideIndex = x.length}
  for (i = 0; i < x.length; i++) {
    x[i].style.display = "none";  
  }
  x[slideIndex-1].style.display = "block";  
}
</script>

</body>
</html>
