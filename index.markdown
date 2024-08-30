---
layout: home
title: Scott Draves
subtitle: Pioneering AI Artist and Engineering Leader
header:
  overlay_image: /assets/img/IMG_8396.jpg
  overlay_filter: 0.5
  actions:
    - label: "Learn More"
      url: "#about"
gallery1:
  - excerpt: Immersive grand opening at 21c Museum Hotel
    image_path: /assets/img/IMG_4507-1024x543.jpg
  - excerpt: Vida retrospective at Espacio Fundación Telefónica, Madrid
    image_path: /assets/img/madrid-vida-retrospective.JPG
  - excerpt: Electric Sheep designed by AI and collective intelligence.
    image_path: /assets/img/IMG_8395-1024x640.jpeg 
gallery2:
  - excerpt: Paul Simon album cover made with Draves' code. 2011.
    image_path: /assets/img/IMG_8310.jpeg
  - excerpt: Stephen Hawking book cover made with Draves' code. 2010.
    image_path: /assets/img/hawking flame.jpg
  - excerpt: At Webster Hall on 50 flat screens. NEW YORK 2009
    image_path: /assets/img/IMG_8308.jpeg
gallery3:
  - excerpt: Skrillex, Grimes, Diplo, Pretty lights with Electric Sheep, summer tour 2012.
    image_path: /assets/img/skrillex-electric-sheep-train-grimes.png
  - excerpt: Dreams in High Fidelity II at Lexus Hybrid Art – MOSCOW 2010
    image_path: /assets/img/draves-moscow-P1000207-888x1024.jpg
---

{% include feature_row id="intro" type="center" %}

<div class="feature__wrapper">
  {% for feature in site.features limit:2 %}
    <div class="feature__item">
      <div class="archive__item">
        <div class="archive__item-teaser">
          <img src="{{ feature.image_path | relative_url }}" alt="{{ feature.alt }}">
        </div>
        <div class="archive__item-body">
          <h2 class="archive__item-title">{{ feature.title }}</h2>
          <div class="archive__item-excerpt">
            {{ feature.excerpt | markdownify }}
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

{% include gallery id="gallery1" caption="Selected Works" %}

{% include testimonials.html %}

<div class="feature__wrapper">
  {% for feature in site.features offset:2 limit:3 %}
    <div class="feature__item">
      <div class="archive__item">
        <div class="archive__item-body">
          <h2 class="archive__item-title">{{ feature.title }}</h2>
          <div class="archive__item-excerpt">
            {{ feature.excerpt | markdownify }}
          </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>
 
{% include gallery id="gallery2" caption="More Works" %}

{% include feature_row id="feature_row2" type="left" %}

{% include gallery id="gallery3" layout="half" caption="Latest Projects" %}