# statistics-slider
In this tutorial, [Solodev](https://www.solodev.com/) demonstrates how to use a Statistics Slider to showcase some important facts you want to convey to your web audience. The slider is built using [Slick Slider](http://kenwheeler.github.io/slick/). 

## Tutorial

For detailed instructions, view Solodev's [Using CSS Transitions and Transforms](https://www.solodev.com/blog/web-design/using-css-transitions-and-transforms.stml) article.

## Demo

Try out a working example on [JSFiddle](https://jsfiddle.net/solodev/86d0wmgj/).

## HTML

Use the following HTML for the tutorial:

```
<div class="ct-current-facts">
  <h2>Company Stats</h2>
  <div class="container">
    <div class="ct-row">
      <div class="ct-current-facts__slider ct-js-current-facts__slider">
        <div class="item">
          <div class="ct-current-fact"><span class="number">#1</span><a href="/district/about-us/" class="title">Ranking in the State</a></div>
        </div>
        <div class="item">
          <div class="ct-current-fact"><span class="number">75</span><a href="/district/about-us/" class="title">On-site Employees</a></div>
        </div>
        <div class="item">
          <div class="ct-current-fact"><span class="number">25<sup></sup></span><a href="/district/about-us/" class="title">Fortune 500 Clients</a></div>
        </div>
        <div class="item">
          <div class="ct-current-fact"><span class="number">7<sup>th</sup></span><a href="/district/about-us/" class="title">Largest in the Nation</a></div>
        </div>
        <div class="item">
          <div class="ct-current-fact"><span class="number">15</span><a href="/district/about-us/" class="title">Years in Business</a></div>
        </div>
        <div class="item">
          <div class="ct-current-fact"><span class="number">12</span><a href="/district/about-us/" class="title">Recent Awards</a></div>
        </div>
      </div>
    </div>
  </div>
</div>
```

## CSS

All required CSS is in statistics-slider.css

## jQuery

Use the following jQuery (also in statistics-slider.js) to initialize the slider

```
'use strict';
(function($) {
  $('document').ready(function() {

    /* Current Facts Slider */
    if ('.ct-js-current-facts__slider'.length) {
      $('.ct-js-current-facts__slider').slick({
        arrows: true,
        slidesToShow: 4,
        autoplay: false,
        prevArrow: '<button type="button" class="slick-arrow slick-arrow--prev">' + '<img src="https://www.solodev.com/assets/statistics-slider/arrow-prev.jpg" />' + '</button>',
        nextArrow: '<button type="button" class="slick-arrow slick-arrow--next">' + '<img src="https://www.solodev.com/assets/statistics-slider/arrow-next.jpg" />' + '</button>',
        responsive: [
          {
            breakpoint: 991,
            settings: {
              slidesToShow: 2
            }
          }, {
            breakpoint: 767,
            settings: {
              slidesToShow: 2
            }
          }, {
            breakpoint: 479,
            settings: {
              slidesToShow: 1
            }
          }
        ]
      });
    }

  });

})(jQuery);
```

## External Includes

This tutorial contains the following third party resources.

```
<link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/slick-carousel/1.6.0/slick.min.css">

<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
<script type="text/javascript" src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
```
