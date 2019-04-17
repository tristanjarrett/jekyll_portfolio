---
layout: snippet
title: Add a progress bar on scroll
slug: progress-bar-on-scroll
author: Tristan Jarrett
date: 2019-04-16 18:30:00 +0000
tags: [JavaScript, CSS, HTML]
---

### Add the following JavaScript

``` JavaScript
window.onscroll = function() {
  myFunction()
};

function myFunction() {
var winScroll = document.body.scrollTop || document.documentElement.scrollTop;
  var height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
  var scrolled = (winScroll / height) * 100;
  document.getElementById("progressBar").style.width = scrolled + "%";
}
```

### Add the following CSS

``` CSS
.progress_container {
  position: absolute;
  width: 100%;
  background: transparent;
}
.progress_bar {
  height: 3px;
  background-color: $primary-color;
  width: 0%;
  max-width: 100%;
}
```
