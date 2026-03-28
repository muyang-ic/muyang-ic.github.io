---
title: "Gallery"
layout: single
author_profile: true
# 下面定义你的图片数组
Japan:
  #- url: /assets/gallery_images/Japan/
  #  image_path: /assets/gallery_images/Japan/
  #  alt: ""
  #  title: ""
  - url: /assets/gallery_images/Japan/fuji_1.jpg
    image_path: /assets/gallery_images/Japan/fuji_1.jpg
    alt: "Fuji"
    title: "Mount Fuji | Lake Yamanaka | Dec 2023"

  - url: /assets/gallery_images/Japan/fuji_2.jpg
    image_path: /assets/gallery_images/Japan/fuji_2.jpg
    alt: "Fuji"
    title: "Mount Fuji & Lawson | Lake Yamanaka | Dec 2023"

  - url: /assets/gallery_images/Japan/akihabara1.jpg
    image_path: /assets/gallery_images/Japan/akihabara1.jpg
    alt: "GTR"
    title: "GTR | Akihabara | Dec 2023"

  - url: /assets/gallery_images/Japan/kamakura_2.jpg
    image_path: /assets/gallery_images/Japan/kamakura_2.jpg
    alt: "Kamakura"
    title: "Kamakura | May 2024"

  - url: /assets/gallery_images/Japan/kanda.jpg
    image_path: /assets/gallery_images/Japan/kanda.jpg
    alt: "Kanda"
    title: "Kanda | Dec 2024"

  - url: /assets/gallery_images/Japan/kokyo.jpg
    image_path: /assets/gallery_images/Japan/kokyo.jpg
    alt: "Kokyo"
    title: "Kokyo | Dec 2024"

  - url: /assets/gallery_images/Japan/shibuya.jpg
    image_path: /assets/gallery_images/Japan/shibuya.jpg
    alt: "Shibuya Crossing"
    title: "Shibuya Crossing | Shibuya | Dec 2023"

  - url: /assets/gallery_images/Japan/ueno_1.jpg
    image_path: /assets/gallery_images/Japan/ueno_1.jpg
    alt: "Uenokoen"
    title: "Torii | Uenokoen | Dec 2024"

  - url: /assets/gallery_images/Japan/ueno_2.jpg
    image_path: /assets/gallery_images/Japan/ueno_2.jpg
    alt: "Uenokoen"
    title: "Torii | Uenokoen | Dec 2024"

  - url: /assets/gallery_images/Japan/utokyo_1.jpg
    image_path: /assets/gallery_images/Japan/utokyo_1.jpg
    alt: "UTokyo"
    title: "UTokyo | Dec 2024"
    
  - url: /assets/gallery_images/Japan/utokyo_2.jpg
    image_path: /assets/gallery_images/Japan/utokyo_2.jpg
    alt: "UTokyo"
    title: "UTokyo | Dec 2024"

  - url: /assets/gallery_images/Japan/ebisu_1.jpg
    image_path: /assets/gallery_images/Japan/ebisu_1.jpg
    alt: "Ebisu"
    title: "Ebisu | Dec 2023"
    
  - url: /assets/gallery_images/Japan/ebisu_2.jpg
    image_path: /assets/gallery_images/Japan/ebisu_2.jpg
    alt: "Night View"
    title: "Tokyo Night View | Ebisu | Dec 2023"

  - url: /assets/gallery_images/Japan/hokaido_1.png
    image_path: /assets/gallery_images/Japan/hokaido_1.png
    alt: "Swan"
    title: "Swan | Kussharoko | Dec 2023"

  - url: /assets/gallery_images/Japan/kamakura_1.jpg
    image_path: /assets/gallery_images/Japan/kamakura_1.jpg
    alt: "Kamakura"
    title: "Kamakura | May 2024"


  
America:
  - url: /assets/gallery_images/America/Colorado_1.jpg
    image_path: /assets/gallery_images/America/Colorado_1.jpg
    alt: "Scrap Car"
    title: "Scrap Car | Colorado | Jul 2024"
    
  - url: /assets/gallery_images/America/Colorado_2.jpg
    image_path: /assets/gallery_images/America/Colorado_2.jpg
    alt: "Rocky Mountain"
    title: "Rocky Mountain | Jul 2024"

  - url: /assets/gallery_images/America/Colorado_3.jpg
    image_path: /assets/gallery_images/America/Colorado_3.jpg
    alt: "Colorado"
    title: "Colorado | Jul 2024"

  - url: /assets/gallery_images/America/Colorado_4.jpg
    image_path: /assets/gallery_images/America/Colorado_4.jpg
    alt: "Colorado"
    title: "Colorado | Jul 2024"

  - url: /assets/gallery_images/America/Colorado_5.jpg
    image_path: /assets/gallery_images/America/Colorado_5.jpg
    alt: "Colorado"
    title: "Colorado | Jul 2024"

  - url: /assets/gallery_images/America/Wyoming_1.jpg
    image_path: /assets/gallery_images/America/Wyoming_1.jpg
    alt: "WYO 230"
    title: "WYO 230 | Wyoming | Jul 2024"

  - url: /assets/gallery_images/America/Wyoming_2.jpg
    image_path: /assets/gallery_images/America/Wyoming_2.jpg
    alt: "GTI"
    title: "GTI | Wyoming | Jul 2024"

  - url: /assets/gallery_images/America/Wyoming_3.jpg
    image_path: /assets/gallery_images/America/Wyoming_3.jpg
    alt: "Billboard"
    title: "Billboard | Wyoming | Jul 2024"

  - url: /assets/gallery_images/America/Wyoming_4.jpg
    image_path: /assets/gallery_images/America/Wyoming_4.jpg
    alt: "Independence Rock"
    title: "Independence Rock | Wyoming | Jul 2024"

  - url: /assets/gallery_images/America/Yellowstone_1.jpg
    image_path: /assets/gallery_images/America/Yellowstone_1.jpg
    alt: "Yellowstone"
    title: "Hiking Trail | Yellowstone | Jul 2024"

  - url: /assets/gallery_images/America/Yellowstone_2.jpg
    image_path: /assets/gallery_images/America/Yellowstone_2.jpg
    alt: "Yellowstone"
    title: "Yellowstone | Jul 2024"
---

<style>
  /* 1. 强制所有图片默认状态：启用硬件加速，开启微小阴影 */
  #my-photography-gallery .gallery-card {
    display: block !important;
    width: 100% !important;
    height: 200px !important;
    border-radius: 6px !important;
    overflow: hidden !important;
    background: #eee !important;
    text-decoration: none !important;
    /* 核心性能：启用 GPU 加速 */
    transform: translateZ(0) !important; 
    will-change: transform, box-shadow !important;
    /* 核心性能：精准的 CSS 过渡，绝不使用 'all' */
    transition: transform 0.2s ease-out !important, box-shadow 0.2s ease-out !important;
    /* 默认加一个极其微弱的阴影，让悬停时的变化更平滑 */
    box-shadow: 0 1px 3px rgba(0,0,0,0.05) !important;
  }

  /* 2. 强制原生 CSS 悬停效果：零延迟反馈 */
  /* 当鼠标悬停在 .gallery-card 上时 */
  #my-photography-gallery .gallery-card:hover {
    transform: translateY(-5px) translateZ(0) !important; /* 微微上浮 */
    box-shadow: 0 10px 20px rgba(0,0,0,0.15) !important; /* 亮起阴影 */
    z-index: 10 !important; /* 确保悬停的图片压住周围图片 */
  }
</style>

I love photography!

<div id="my-photography-gallery">

  ### Japan
  <div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); gap: 15px; margin-bottom: 40px;">
    {% for img in page.Japan %}
    <a href="{{ img.url }}" class="image-popup gallery-card" title="{{ img.title }}">
      <img src="{{ img.image_path }}" alt="{{ img.alt }}" loading="lazy" decoding="async" style="width: 100%; height: 100%; object-fit: cover; margin: 0; display: block;" />
    </a>
    {% endfor %}
  </div>

  ### America
  <div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(180px, 1fr)); gap: 15px; margin-bottom: 40px;">
    {% for img in page.America %}
    <a href="{{ img.url }}" class="image-popup gallery-card" title="{{ img.title }}">
      <img src="{{ img.image_path }}" alt="{{ img.alt }}" loading="lazy" decoding="async" style="width: 100%; height: 100%; object-fit: cover; margin: 0; display: block;" />
    </a>
    {% endfor %}
  </div>

</div>