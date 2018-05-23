---
layout: post
title: Jekyll Customization
categories: Misc
---

It would be nice to have some way to categorize blog posts.  This looks like an interesting link: [3 Simple Steps To Setup Jekyll Categories And Tags](https://blog.webjeda.com/jekyll-categories/)

First piece of the puzzle: [categories](https://shannonscott.github.io/categories/)

Still working on the rest.

<div class="post-categories">
  {% if post %}
    {% assign categories = post.categories %}
  {% else %}
    {% assign categories = page.categories %}
  {% endif %}
  Filed under:
  {% for category in categories %}
  <a href="{{site.baseurl}}/categories/#{{category|slugize}}">{{category}}</a>
  {% unless forloop.last %}&nbsp;{% endunless %}
  {% endfor %}
</div>
