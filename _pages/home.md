---
title: "Intellimaging Tech - Home"
layout: homelay
excerpt: "Developing artificial intelligence technologies for medical imaging"
sitemap: false
permalink: /
---
<html>

<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
* {box-sizing: border-box;}

.img-magnifier-container {
  position:relative;
}

.img-magnifier-glass {
  position: absolute;
  border: 3px solid #000;
  border-radius: 50%;
  cursor: none;
  /*Set the size of the magnifier glass:*/
  width: 100px;
  height: 100px;
}
</style>
<script>
function magnify(imgID, zoom) {
  var img, glass, w, h, bw;
  img = document.getElementById(imgID);
  /*create magnifier glass:*/
  glass = document.createElement("DIV");
  glass.setAttribute("class", "img-magnifier-glass");
  /*insert magnifier glass:*/
  img.parentElement.insertBefore(glass, img);
  /*set background properties for the magnifier glass:*/
  glass.style.backgroundImage = "url('" + img.src + "')";
  glass.style.backgroundRepeat = "no-repeat";
  glass.style.backgroundSize = (img.width * zoom) + "px " + (img.height * zoom) + "px";
  bw = 3;
  w = glass.offsetWidth / 2;
  h = glass.offsetHeight / 2;
  /*execute a function when someone moves the magnifier glass over the image:*/
  glass.addEventListener("mousemove", moveMagnifier);
  img.addEventListener("mousemove", moveMagnifier);
  /*and also for touch screens:*/
  glass.addEventListener("touchmove", moveMagnifier);
  img.addEventListener("touchmove", moveMagnifier);
  function moveMagnifier(e) {
    var pos, x, y;
    /*prevent any other actions that may occur when moving over the image*/
    e.preventDefault();
    /*get the cursor's x and y positions:*/
    pos = getCursorPos(e);
    x = pos.x;
    y = pos.y;
    /*prevent the magnifier glass from being positioned outside the image:*/
    if (x > img.width - (w / zoom)) {x = img.width - (w / zoom);}
    if (x < w / zoom) {x = w / zoom;}
    if (y > img.height - (h / zoom)) {y = img.height - (h / zoom);}
    if (y < h / zoom) {y = h / zoom;}
    /*set the position of the magnifier glass:*/
    glass.style.left = (x - w) + "px";
    glass.style.top = (y - h) + "px";
    /*display what the magnifier glass "sees":*/
    glass.style.backgroundPosition = "-" + ((x * zoom) - w + bw) + "px -" + ((y * zoom) - h + bw) + "px";
  }
  function getCursorPos(e) {
    var a, x = 0, y = 0;
    e = e || window.event;
    /*get the x and y positions of the image:*/
    a = img.getBoundingClientRect();
    /*calculate the cursor's x and y coordinates, relative to the image:*/
    x = e.pageX - a.left;
    y = e.pageY - a.top;
    /*consider any page scrolling:*/
    x = x - window.pageXOffset;
    y = y - window.pageYOffset;
    return {x : x, y : y};
  }
}
</script>
</head>
    
<body>
<p style="text-align: justify;">Artificial Intelligence (AI) is revolutionizing medical imaging by enhancing diagnostic precision, streamlining workflow efficiency, and enabling early disease detection. Leveraging machine learning (ML) and deep learning (DL) techniques, AI-driven tools interpret complex medical images—such as MRIs, CT scans, and ultrasounds—transforming radiology and extending its reach across healthcare. These tools expertly identify abnormalities like tumors, fractures, and infections, while supporting early detection of cancers, cardiovascular diseases, and neurological disorders. AI accurately delineates anatomical structures and lesions, facilitating surgical planning, radiation therapy, and other interventions. Additionally, it distinguishes benign from malignant lesions, categorizes disease subtypes, informs personalized treatment strategies, and measures tumor volume, organ size, and vascular characteristics while tracking disease progression and treatment response. Specializing in X-ray tomographic imaging, photoacoustic imaging, and advanced image reconstruction and analysis, we are developing innovative theories, methods, software, and hardware systems for clinical use in disease detection and diagnosis. We welcome collaboration with partners and funding agencies on transformative, high-impact projects.</p>

<div markdown="0" id="carousel" class="carousel slide" data-ride="carousel" data-interval="2500" data-pause="hover" >
    <!-- Menu
    <ol class="carousel-indicators">
        <li data-target="#carousel" data-slide-to="0" class="active"></li>
        <li data-target="#carousel" data-slide-to="1"></li>
        <li data-target="#carousel" data-slide-to="2"></li>
        <li data-target="#carousel" data-slide-to="3"></li>
    </ol> -->

    <!-- Items -->
    <div class="carousel-inner" markdown="0">
    
        <div class="item active">
            <a href="{{ site.url }}{{ site.baseurl }}/images/Slide1.PNG">
              <img src="{{ site.url }}{{ site.baseurl }}/images/Slide1.PNG" alt="Slide 1" width="800" height="600"/>
            </a>
        </div>

        <!-- Second Slide -->
        <!--<div class="item">-->
        <div class="img-zoom-container">
            <a href="{{ site.url }}{{ site.baseurl }}/images/Slide000.png">
                <img src="{{ site.url }}{{ site.baseurl }}/images/Slide000.png" alt="Slide 2" width="800" height="600"/>
            </a>
        </div>

        <!-- Third Slide -->
        <div class="item">
            <a href="{{ site.url }}{{ site.baseurl }}/images/Slide11.png">
                <img id="img1" src="{{ site.url }}{{ site.baseurl }}/images/Slide11.png" onclick="enlargeImg(this.id)" alt="Slide 3" width="800" height="600"/>
            </a>
        </div>

        <!-- Fourth Slide -->
        <div class="item">
            <a href="{{ site.url }}{{ site.baseurl }}/images/Slide3.png" >
                <img src="{{ site.url }}{{ site.baseurl }}/images/Slide3.png" alt="Slide 4" width="800" height="600"/>
            </a>
        </div>
  </div>
  <!--
  <a class="left carousel-control" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">Next</span> 
  </a>
  -->
  <!--
  <a class="left carousel-control" role="button" data-slide="prev" onclick="moveCarousel('prev')">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" role="button" data-slide="next" onclick="moveCarousel('next')">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
  -->
</div>

<!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
<!-- Include all compiled plugins (below), or include individual files as needed -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

</body>
</html>
