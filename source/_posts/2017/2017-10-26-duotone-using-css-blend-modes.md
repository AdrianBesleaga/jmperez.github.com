---
layout: post
title: Duotone using CSS blend modes
date: 2017-10-26 08:15:00+02:00
description: Using CSS blend modes to apply a duotone effect to an image.
image:
  url: /assets/images/posts/duotone.jpg
  width: 887
  height: 501
tags:
  - svg
permalink: duotone-using-css-blend-modes
---

In a past post I explained [how to use SVG and a `feColorMatrix` filter](/duotone-using-fecolormatrix) to apply a duotone effect to an image. This time I'm going to show how to achieve a similar effect with only CSS.

<!-- more -->
Demo & Code: [https://codepen.io/jmperez/pen/wrVxga](http://codepen.io/jmperez/pen/wrVxga)


<p data-height="367" data-theme-id="0" data-slug-hash="wrVxga" data-default-tab="result" data-user="jmperez" class='codepen'>See the Pen <a href='http://codepen.io/jmperez/pen/wrVxga/'>Duotone effect (Spotify Duotone) - Using CSS blend modes</a> by José Manuel Pérez (<a href='http://codepen.io/jmperez'>@jmperez</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

The code consists of a `<div/>` that has an image set as a background. Then, we add a `::before` and an `::after` pseudo-elements with the colours we want to apply and the right blend modes.

Previously, my colleague Thodoris described how to achieve this effect [in JS using Canvas](http://blog.72lions.com/blog/2015/7/7/duotone-in-js) and [in iOS](http://blog.72lions.com/blog/2015/7/18/duotone-in-ios). I also reproduced it using [SVG and a `feColorMatrix` filter](/duotone-using-fecolormatrix).

This version is based on the technique described by Una Kravets:

<blockquote class="twitter-tweet" data-lang="en-gb"><p lang="en" dir="ltr">Duotone images are so <a href="https://twitter.com/hashtag/trendy?src=hash&amp;ref_src=twsrc%5Etfw">#trendy</a> right now 😎<br><br>Had some airport time so I drew out how to get this effect w/one div in CSS 😊 <a href="https://twitter.com/hashtag/devdoodles?src=hash&amp;ref_src=twsrc%5Etfw">#devdoodles</a> <a href="https://t.co/WENOWlwcUY">pic.twitter.com/WENOWlwcUY</a></p>&mdash; Una Kravets 👩🏻‍💻 (@Una) <a href="https://twitter.com/Una/status/923231326420922368?ref_src=twsrc%5Etfw">25 October 2017</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

which is also what the [colofilter.css](http://lukyvj.github.io/colofilter.css/) library is based on to achieve the duotone effect.
