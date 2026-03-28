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

This is a gallery of my photography works

{% include gallery id="Japan" caption="Japan" %}
{% include gallery id="America" caption="America" %}

<style>
  /* 专门针对 gallery 里的图片强制统一尺寸 */
  .gallery img {
    height: 200px;       /* 网格高度 */
    width: 100%;         /* 强制宽度占满它所在的列 */
    object-fit: cover;   /* 填满 */
    border-radius: 6px;  /* 圆角 */
  }
</style>