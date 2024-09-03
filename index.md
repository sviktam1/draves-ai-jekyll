---
layout: home
author_profile: true
author: Scott Draves
subtitle: Pioneering AI Artist and Engineering Leader
header:
  image: /assets/img/IMG_8396.jpg
gallery1:
  - excerpt: Immersive grand opening at 21c Museum Hotel
    image_path: /assets/img/IMG_4507-1024x543.jpg
  - excerpt: Vida retrospective at Espacio Fundación Telefónica, Madrid
    image_path: /assets/img/madrid-vida-retrospective.JPG
gallery2:
  - excerpt: Electric Sheep designed by AI and collective intelligence.
    image_path: /assets/img/IMG_8395-1024x640.jpeg 
gallery3:
  - excerpt: Paul Simon album cover made with Draves' code. 2011.
    image_path: /assets/img/IMG_8310.jpeg
  - excerpt: Stephen Hawking book cover made with Draves' code. 2010.
    image_path: /assets/img/hawking flame.jpg
  - excerpt: At Webster Hall on 50 flat screens. NEW YORK 2009
    image_path: /assets/img/IMG_8308.jpeg
  - excerpt: Skrillex, Grimes, Diplo, Pretty lights with Electric Sheep, summer tour 2012.
    image_path: /assets/img/skrillex-electric-sheep-train-grimes.png
gallery4:
  - excerpt: Dreams in High Fidelity II at Lexus Hybrid Art – MOSCOW 2010
    image_path: /assets/img/draves-moscow-P1000207-888x1024.jpg
---

<div class="feature__wrapper custom-features custom-features-first" data-aos="fade-up">
  {% for feature in site.features limit:2 %}
    <div class="feature__item custom-feature">
      <div class="archive__item">
        <div class="archive__item-icon">
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

<div class="figure-row figure-row-two" data-aos="fade-up" data-aos-delay="100">
  {% for item in page.gallery1 %}
    <figure class="image-hover-effect" data-aos="zoom-in" data-aos-delay="{{ forloop.index | times: 100 }}">
      <a href="{{ item.image_path }}" class="image-popup" title="{{ item.excerpt }}">
        <img src="{{ item.image_path }}" alt="{{ item.excerpt }}">
        <figcaption>
          <p>{{ item.excerpt }}</p>
        </figcaption>
      </a>
    </figure>
  {% endfor %}
</div>


{% include testimonials.html %}


<div class="feature__wrapper custom-features" data-aos="fade-up" data-aos-delay="200">
   {% for feature in site.features offset:2 limit:3 %}
    <div class="feature__item custom-feature">
      <div class="archive__item">
        <div class="archive__item-icon">
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


<div class="testimonials-gallery-row" data-aos="fade-up" data-aos-delay="300">
  {% for item in page.gallery2 limit:1 %}
      <div class="gallery-column">
      {% include figure popup=true image_path=item.image_path alt=item.excerpt caption=item.excerpt %}
  </div>
  {% endfor %}
  <div class="testimonials-column">
    {% for testimonial in site.data.testimonials offset:2 limit:2 %}
      <blockquote class="testimonial">
        <p>{{ testimonial.quote }}</p>
        <cite>{{ testimonial.author }}</cite>
      </blockquote>
    {% endfor %}
  </div>
</div>




<div class="figure-row" data-aos="fade-up" data-aos-delay="400">
  {% for item in page.gallery3 %}
    <figure class="image-hover-effect" data-aos="flip-left" data-aos-delay="{{ forloop.index | times: 100 }}">
      <a href="{{ item.image_path }}" class="image-popup" title="{{ item.excerpt }}">
        <img src="{{ item.image_path }}" alt="{{ item.excerpt }}">
        <figcaption>
          <p>{{ item.excerpt }}</p>
        </figcaption>
      </a>
    </figure>
  {% endfor %}
</div>

<div class="figure-row-horizontal" data-aos="fade-up" data-aos-delay="500">
  {% for item in page.gallery4 limit:1 %}
    <figure>
      <div class="horizontal-image-container">
        <a href="{{ item.image_path }}" class="image-popup" title="{{ item.excerpt }}">
          <img src="{{ item.image_path }}" alt="{{ item.excerpt }}" class="horizontal-image">
        </a>
      </div>
      <figcaption>{{ item.excerpt }}</figcaption>
    </figure>
  {% endfor %}
</div>