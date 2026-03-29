---
title: "Gallery"
layout: single
author_profile: true
permalink: /gallery/
---

This is a collection of my photography works. Select an album to explore.

<style>
  /* 专属毛玻璃导航卡片样式 */
  .category-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* 自动响应式，大屏并排，小屏上下 */
    gap: 25px;
    margin-top: 30px;
  }
  
  .category-card {
    position: relative;
    height: 250px; /* 封面卡片的高度 */
    border-radius: 12px;
    overflow: hidden;
    text-decoration: none !important;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    transform: translateZ(0); /* 开启硬件加速 */
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .category-card:hover {
    transform: translateY(-8px); /* 悬停时卡片整体上浮 */
    box-shadow: 0 15px 30px rgba(0,0,0,0.2);
  }

  /* 提取你最满意的一张照片作为底层背景，并进行轻度模糊 */
  .category-bg {
    position: absolute;
    top: -10px; left: -10px; right: -10px; bottom: -10px; /* 放大一点以防边缘漏光 */
    background-size: cover;
    background-position: center;
    filter: blur(4px) brightness(0.9); /* 底层模糊和压暗 */
    transition: transform 0.5s ease;
    z-index: 1;
  }
  
  .category-card:hover .category-bg {
    transform: scale(1.08); /* 悬停时背景缓慢放大，高级感来源 */
  }

  /* 最核心的毛玻璃文字层 */
  .category-content {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 2;
    background: rgba(255, 255, 255, 0.1); /* 覆盖一层极淡的白底 */
    backdrop-filter: blur(8px); /* 真正的毛玻璃滤镜 */
    -webkit-backdrop-filter: blur(8px); /* 兼容 Safari 浏览器 */
  }

  .category-content h2 {
    color: white;
    font-size: 2.0rem;
    font-weight: bold;
    margin: 0;
    text-shadow: 0 2px 10px rgba(0,0,0,0.5); /* 给文字加上黑阴影防止看不清 */
    letter-spacing: 3px;
    /*text-transform: uppercase;*/ /* 强制大写显得更专业 */
  }
</style>

<div class="category-grid">
  <a href="/japan/" class="category-card">
    <div class="category-bg" style="background-image: url('/assets/gallery_images/Japan/fuji_1.jpg');"></div>
    <div class="category-content">
      <h2>Japan</h2>
    </div>
  </a>

  <a href="/america/" class="category-card">
    <div class="category-bg" style="background-image: url('/assets/gallery_images/America/Yellowstone_1.jpg');"></div>
    <div class="category-content">
      <h2>America</h2>
    </div>
  </a>
</div>