---
layout: splash
author_profile: true
author: Scott Draves
subtitle: Pioneering AI Artist & Engineering Leader
classes: wide
header:
  image: /assets/img/IMG_8396.jpg
gallery1:
  - excerpt: Immersive grand opening at 21c Museum Hotel, Bentonville 2013
    image_path: /assets/img/IMG_4507-1024x543.jpg
  - excerpt: Vida retrospective at Espacio Fundación Telefónica, Madrid 2012
    image_path: /assets/img/madrid-vida-retrospective.JPG
gallery2:
  - excerpt: Electric Sheep designed by collective intelligence of AI and human artists
    image_path: /assets/img/IMG_8395-1024x640.jpeg 
gallery3:
  - excerpt: Paul Simon album cover made with Draves' code, 2011
    image_path: /assets/img/IMG_8310.jpeg
  - excerpt: Stephen Hawking book cover made with Draves' code, 2010
    image_path: /assets/img/hawking flame.jpg
  - excerpt: At Webster Hall on 50 flat screens, New York 2009
    image_path: /assets/img/IMG_8308.jpeg
  - excerpt: Skrillex, Grimes, Diplo, Pretty lights with Electric Sheep, summer tour 2012
    image_path: /assets/img/skrillex-electric-sheep-train-grimes.png
gallery4:
  - excerpt: Opening night of Lexus Hybrid Art, Moscow 2010
    image_path: /assets/img/draves-moscow-P1000207-888x1024.jpg
links:
  - label: "LinkedIn"
    icon: "fab fa-fw fa-linkedin"
    url: "https://www.linkedin.com/in/scottdraves"
  - label: "Threads"
    icon: "fab fa-fw fa-threads"
    url: "https://www.threads.net/@scott__draves"
  - label: "Facebook"
    icon: "fab fa-fw fa-facebook"
    url: "https://www.facebook.com/scott.draves"
  - label: "Twitter"
    icon: "fab fa-fw fa-twitter-square"
    url: "https://twitter.com/scott_draves?lang=en"
  - label: "Instagram"
    icon: "fab fa-fw fa-instagram"
    url: "https://www.instagram.com/scott__draves/"
  - label: "YouTube"
    icon: "fab fa-fw fa-youtube"
    url: "https://www.youtube.com/@ScottDraves"
  - label: "GitHub"
    icon: "fab fa-fw fa-github"
    url: "https://github.com/scottdraves"
---

<div> 
  <img class="author__avatar-img" src="/assets/img/face.jpg" alt="Author">
</div>

<div class="feature__wrapper custom-features custom-features-first" data-aos="fade-up">
  {% for feature in site.features limit:3 %}
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

<div class="figure-row figure-row-two d-flex" data-aos="fade-up" data-aos-delay="100">
  {% for item in page.gallery1 %}
    <div style="max-width: 450px">
      <figure class="" style="max-width: 100%; height: 320px" data-aos="zoom-in" data-aos-delay="{{ forloop.index | times: 100 }}">
        <a href="{{ item.image_path }}" class="image-popup" title="{{ item.excerpt }}">
          <img style="width: 100%; height: 350px" src="{{ item.image_path }}" alt="{{ item.excerpt }}">
        </a>
      </figure>
      <figcaption style="width: fit-content;">
        <p style="width: fit-content;">{{ item.excerpt }}</p>
      </figcaption>
    </div>
  {% endfor %}
</div>


{% include testimonials.html %}


<div class="feature__wrapper custom-features" data-aos="fade-up" data-aos-delay="200">
   {% for feature in site.features offset:3 limit:5 %}
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

<div class="figure-row d-flex" data-aos="fade-up" data-aos-delay="400">
  {% for item in page.gallery3 %}
    <div style="max-width: 215px">
      <figure class="" style="max-width: 100%; height: 170px" data-aos="flip-left" data-aos-delay="{{ forloop.index | times: 100 }}">
        <a href="{{ item.image_path }}" class="image-popup" title="{{ item.excerpt }}">
          <img style="height: 200px" src="{{ item.image_path }}" alt="{{ item.excerpt }}">
        </a>
      </figure>
      <figcaption style="width: fit-content;">
        <p style="width: fit-content;">{{ item.excerpt }}</p>
      </figcaption>
    </div>
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

<div class="figure-row-horizontal" data-aos="fade-up" data-aos-delay="500">
  <div class="author__urls social-icons">
  {% for link in page.links %}
    {% if link.label and link.url %}
       <a href="{{ link.url }}" rel="nofollow noopener noreferrer me"{% if link.url contains 'http' %} itemprop="sameAs"{% endif %}><i class="{{ link.icon | default: 'fas fa-link' }}" aria-hidden="true"></i><span class="label">{{ link.label }}</span></a>
    {% endif %}
  {% endfor %}
  </div>
</div>
