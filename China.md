---
title: "China"
layout: single
author_profile: true
permalink: /china/
China:
  - url: /assets/gallery_images/China/Cat_1.jpg
    image_path: /assets/gallery_images/China/Cat_1.jpg
    alt: "cat"
    title: "Cat | Shanghai | Dec 2025"

  - url: /assets/gallery_images/China/Cat_2.jpg
    image_path: /assets/gallery_images/China/Cat_2.jpg
    alt: "cat"
    title: "Cat | Shanghai | Dec 2025"

  - url: /assets/gallery_images/China/Cat_3.jpg
    image_path: /assets/gallery_images/China/Cat_3.jpg
    alt: "cat"
    title: "Cat | Shanghai | Dec 2025"

  - url: /assets/gallery_images/China/Huangshan.jpg
    image_path: /assets/gallery_images/China/Huangshan.jpg
    alt: "huangshan"
    title: "Huangshan | Anhui | Jan 2026"

  - url: /assets/gallery_images/China/Hunan_3.jpg
    image_path: /assets/gallery_images/China/Hunan_3.jpg
    alt: "hunan"
    title: "Hunan | Jul 2024"

  - url: /assets/gallery_images/China/Hunan_2.jpg
    image_path: /assets/gallery_images/China/Hunan_2.jpg
    alt: "hunan"
    title: "Hunan | Jul 2024"

  - url: /assets/gallery_images/China/MilkyWay.jpg
    image_path: /assets/gallery_images/China/MilkyWay.jpg
    alt: "milkyway"
    title: "MilkyWay | Chongming | Aug 2023"

---

<p><a href="/gallery/" style="text-decoration: none; font-weight: bold; ">&larr; Back to Gallery</a></p>

<style>
  #my-photography-gallery .gallery-card {
    position: relative !important; display: block !important; width: 100% !important; height: 200px !important;
    border-radius: 6px !important; overflow: visible !important; background: #eee !important;
    text-decoration: none !important; transition: none !important; 
  }
  #my-photography-gallery .gallery-card img {
    width: 100% !important; height: 100% !important; object-fit: cover !important; border-radius: 6px !important; 
    position: relative !important; z-index: 2 !important;
  }
  #my-photography-gallery .gallery-card::after {
    content: '' !important; position: absolute !important; inset: 0 !important; border-radius: 6px !important;
    box-shadow: 0 5px 15px rgba(0,0,0,0.2) !important; opacity: 0 !important; 
    transition: opacity 0.2s ease-out !important; z-index: 1 !important; pointer-events: none !important;
  }
  #my-photography-gallery .gallery-card:hover { z-index: 10 !important; }
  #my-photography-gallery .gallery-card:hover::after { opacity: 1 !important; }
</style>

<div id="my-photography-gallery">
  <div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); gap: 15px; margin-bottom: 40px;">
    {% for img in page.China %}
    <a href="{{ img.url }}" class="image-popup gallery-card" title="{{ img.title }}">
      <img src="{{ img.image_path }}" alt="{{ img.alt }}" loading="lazy" decoding="async" style="width: 100%; height: 100%; object-fit: cover; margin: 0; display: block;" />
    </a>
    {% endfor %}
  </div>
</div>