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

{% include gallery id="gallery2" caption="More Works" %}

{% include feature_row id="feature_row2" type="left" %}

{% include gallery id="gallery3" layout="half" caption="Latest Projects" %}