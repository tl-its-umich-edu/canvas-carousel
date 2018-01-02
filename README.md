# canvas-carousel
Revolving slide carousel that runs on Canvas home page

# canvas-carousel
Revolving slide carousel that runs on Canvas home page

The carousel is enabled by inseting a script in the custom theme editor of Canvas that luanches the slides in an iframe of the Canvas home page (also referred to as Canvas Dashboard):
```
$( document ).ready(function() {
  // Add Carousel
  $( "#dashboard" ).before("<iframe src='https://path_to_your_carousel' width='850' height='173' frameBorder='0' role='complementary' ></iframe>");
});
```

You can add slide content by adding an image, link, alt tag, and accessible caption as a list item in the unordered list commented as "Wrapper for slides" in the canvas_carousel_player.html file:
```
<!-- Wrapper for slides -->
  <ul class="carousel-inner hidden-xs">
    <!-- first slide -->
    <li class="item active"> <img src="https://some_image.gif" alt="alt text here" onclick="window.open('http://some_url')">
      <h3 class="carousel-caption sr-only" id="carousel-caption1">caption for screen readers here</h3>
    </li>
    <!-- second slide -->
    <li class="item active"> <img src="https://some_image.gif" alt="alt text here" onclick="window.open('http://some_url')">
      <h3 class="carousel-caption sr-only" id="carousel-caption1">caption for screen readers here</h3>
    </li>
  </ul>
```
