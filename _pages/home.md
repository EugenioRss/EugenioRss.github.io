---
layout: splash
permalink: /
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: https://res.cloudinary.com/eugenio-rossini/image/upload/v1657821042/theWineCellarMusic/home_wallpaper.jpg
excerpt: "Bacon ipsum dolor sit amet salami ham hock ham, hamburger corned beef short ribs kielbasa biltong t-bone drumstick tri-tip tail sirloin pork chop."
---
**Recent Posts:**
{% if post.header.teaser %}
  {% capture teaser %}{{ post.header.teaser }}{% endcapture %}
{% else %}
  {% assign teaser = site.teaser %}
{% endif %}

<div class="feature__wrapper">
   {% for post in site.posts limit:5 %}
   <div class="feature__item">
      <div class="archive__item">
         <div class="archive__item-teaser">
            <a href="{{ post.url | relative_url }}"><img src="{{ post.header.teaser | relative_url }}" alt="{{ post.title }}"></a>
         </div>
         <div class="archive__item-body">
            <h3 class="archive__item-title"><a href="{{ site.baseurl }}{{ post.url}}" rel="permalink">{{ post.title }}</a></h3>
            <div class="archive__item-excerpt">
               <p>{% if post.excerpt %}<p class="archive__item-excerpt" itemprop="description">{{ post.excerpt | markdownify | strip_html | truncate: 160}}[&nbsp;<a href="{{ post.url | relative_url }}">Read&nbsp;More...</a>&nbsp;]</p>{% endif %}</p>
            </div>
         </div>
      </div>
   </div>
   {% endfor %}
</div>