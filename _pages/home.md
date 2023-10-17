---
layout: splash
permalink: /
header:
  overlay_color: "#000"
  overlay_filter: "0.3"
  overlay_image: https://res.cloudinary.com/eugenio-rossini/image/upload/t_Rounded 4:3/v1697454282/theWineCellarMusic/High-quality-image-of-a-cozy-room-with-warm-light-that-contains-a-large-vinyl-records-collection-and-Hi-Fi-stereo--The-image-should-contains-also-aspect-of-young--rebel--and-catchy-_rgespj.png
excerpt: |+
    "I'm very good at the past. It's the present I can't understand."


    *Nick Hornby, High Fidelity*


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