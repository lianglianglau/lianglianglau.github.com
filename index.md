---
layout: page
title: Be a Simple men!
tagline: Supporting tagline
---
{% include JB/setup %}



## Some Words to Myself

- 做人，不能过盛，得意时兀凌人，处高时莫自居，喜怒勿形于色，成败内敛于胸；
不能过怨，能甘于檐下，可远离尘世，得失皆身外，是非置脑后；
不能过衰，清不避浊，浑能扬清，不弃为人原则，固守尊严底线。
- 程序人生


## My Post List 我的文章列表

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>




