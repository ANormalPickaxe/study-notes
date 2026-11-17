---
layout: home
title: My Study Notes
permalink: /  # 设置为根目录地址
---

<div class="home">
  
  <!-- 主要内容区域 -->
  <main class="content">
    <h1 class="page-heading">My Study Notes</h1>
    
    <!-- 侧边栏：列出所有笔记 -->
    <aside class="sidebar">
      <h2>笔记目录</h2>
      <ul>
        {% for post in site.posts %}
          <li>
            <a href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
            <span>{{ post.date | date: "%Y-%m-%d" }}</span>
          </li>
        {% endfor %}
      </ul>
    </aside>
    
    <!-- 这里可以写一些欢迎语或简介 -->
    <h2>欢迎来到我的学习笔记网页。</h2>
    <div class="post-list">
      {% for post in site.posts limit: 3 %}
        <h3><a href="{{ post.url }}">{{ post.title }}</a></h3>
        <small>{{ post.date | date: "%Y-%m-%d" }}</small>
        <p>{{ post.excerpt }}</p>
      {% endfor %}
    </div>
  </main>
  
</div>