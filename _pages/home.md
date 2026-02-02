---
title: "Intellimaging Tech - Home"
layout: homelay
excerpt: "Developing artificial intelligence technologies for medical imaging"
sitemap: false
permalink: /
---
<html>    
     <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zoom Image on Link Click</title>
    <style>
        /* Container for links */
        .link-container {
            padding: 20px;
        }

        /* Styling for links */
        .image-link {
            display: block;
            margin: 10px 0;
            text-decoration: none;
            color: #007BFF;
            cursor: pointer;
        }

        .image-link:hover {
            text-decoration: underline;
        }

        /* Modal (fixed window) styling */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .modal-content {
            position: relative;
            text-align: center;
        }

        .modal-image {
            max-width: 80%;
            max-height: 70vh;
            transition: transform 0.3s ease;
            cursor: pointer;
        }

        .zoomed {
            transform: scale(2); /* 2x zoom */
        }

        .close {
            position: absolute;
            top: 20px;
            right: 30px;
            color: white;
            font-size: 40px;
            cursor: pointer;
        }
    </style>
</head>

<body>
<p style="text-align: justify;"> Artificial Intelligence (AI) is revolutionizing medical imaging by enhancing diagnostic precision, streamlining workflows, and enabling earlier disease detection. By leveraging machine learning and deep learning techniques, AI tools can interpret complex data from MRIs, CT scans, and ultrasounds with unprecedented accuracy. These advancements allow for the precise identification of abnormalities, such as tumors and lesions, while facilitating surgical planning and personalized treatment strategies.<br>
<br>
Building on this technological shift, our team specializes in X-ray tomographic imaging, photoacoustic imaging, and advanced image reconstruction. We are developing innovative imaging models, software, and hardware systems designed for clinical use. We actively welcome collaboration with partners and funding agencies on transformative, high-impact projects that expand the capabilities of disease detection and diagnosis.</p>
<br>
<div class="image-gallery"> 
     <a href="#" onclick="openModal('{{ site.url }}{{ site.baseurl }}/images/Slide1.PNG', 'Image1')">
     <img class="mySlides" src="{{ site.url }}{{ site.baseurl }}/images/Slide1.PNG" style="width:100%"/></a>
     <a href="#" onclick="openModal('{{ site.url }}{{ site.baseurl }}/images/MRI-3.png', 'Image2')">
     <img class="mySlides" src="{{ site.url }}{{ site.baseurl }}/images/MRI-3.png" style="width:100%"/></a>
     <a href="#" onclick="openModal('{{ site.url }}{{ site.baseurl }}/images/Slide-OA-2.png', 'Image3')">
     <img class="mySlides" src="{{ site.url }}{{ site.baseurl }}/images/Slide-OA-2.png" style="width:100%"/></a>
     <a href="#" onclick="openModal('{{ site.url }}{{ site.baseurl }}/images/Slide-US-2.png', 'Image4')">
     <img class="mySlides" src="{{ site.url }}{{ site.baseurl }}/images/Slide-US-2.png" style="width:100%"/></a>
     <a href="#" onclick="openModal('{{ site.url }}{{ site.baseurl }}/images/Slide11.png', 'Image5')">
     <img class="mySlides" src="{{ site.url }}{{ site.baseurl }}/images/Slide11.png" style="width:100%"/></a>
</div>
<br>
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

<!-- Modal (fixed window) -->
<div class="modal" id="imageModal">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">×</span>
        <img id="modalImage" class="modal-image" onclick="toggleZoom(this)">
    </div>
</div>

<script>
    // Open modal with the linked image
    function openModal(imgSrc, imgAlt) {
        const modal = document.getElementById('imageModal');
        const modalImage = document.getElementById('modalImage');
        modalImage.src = imgSrc;
        modalImage.alt = imgAlt;
        modalImage.classList.remove('zoomed'); // Reset zoom
        modal.style.display = 'flex';
    }

    // Close modal
    function closeModal() {
        document.getElementById('imageModal').style.display = 'none';
    }

    // Toggle zoom on click
    function toggleZoom(image) {
        image.classList.toggle('zoomed');
    }

    // Close modal when clicking outside the image
    document.getElementById('imageModal').onclick = function(e) {
        if (e.target === this) closeModal();
    };
</script>

</body>
</html>
