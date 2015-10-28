---
layout: post
title:  "CSS Stacked Paper Effect"
---
Heads up: this is more of an experiment than something that would be used in production.

See it in [action here](http://codepen.io/alexpate/pen/MwjMxP).

{% highlight html %}
<div class="paper">
</div>
{% endhighlight %}

{% highlight scss %}
.paper {
  background: #fff;
  box-shadow: 0 0 2px rgba(0, 0, 0, .34);
  height: 400px;
  margin: 50px auto 0 auto;
  position: relative;
  width: 450px;

  &:before,
  &:after {
    background: #fff;
    box-shadow: 0 0 2px rgba(0, 0, 0, .34);
    content: '';
    height: 100%;
    position: absolute;
    transform: rotate(3deg);
    transition: all .3s ease-in-out;
    width: 100%;
    z-index:-1;
  }

  &:after {
    box-shadow: 0 0 2px rgba(0, 0, 0, .34);
    left: 0;
    top: 0;
    transform: rotate(1deg);
  }

  &:hover:after,
  &:hover:before {
    box-shadow: none;
    transform: rotate(0deg);
  }

}

{% endhighlight %}
