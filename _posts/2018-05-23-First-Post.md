---
layout: post
title: Initial post
categories: Misc Jekyll
---

I am trying out [Jekyll-Now](https://github.com/barryclark/jekyll-now) on [Github](https://github.com) as a quick and easy way to blog.  We'll see how well this works in practice.

This article was helpful getting things setup: [Build A Blog With Jekyll And GitHub Pages](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)

# Old stuff

Leaving this here for a bit.

![_config.yml]({{ site.baseurl }}/images/config.png)

<div class="post-categories">
  {% if post %}
    {% assign categories = post.categories %}
  {% else %}
    {% assign categories = page.categories %}
  {% endif %}
  {% for category in categories %}
  <a href="{{site.baseurl}}/categories/#{{category|slugize}}">{{category}}</a>
  {% unless forloop.last %}&nbsp;{% endunless %}
  {% endfor %}
</div>

