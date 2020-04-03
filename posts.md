---
layout: page
title: "Posts"
permalink: /posts/
main_nav: true
---

Welcome to Nescient Musings. This is the beginnings of my blog.
I heard that you become who you tell yourself you are.
That narratives, usually false, constructed about who we are steer us in who we become.
What a neat thought.
The purpose of this blog is to serve me as a chronicle of thoughts and ideas 
that would interest the person I want to become and (with luck) some that I hope will stay with me forever.

If by any chance, you are not future me, know that I am pleasantly delighted and hope you find some of these posts worth their reading time. 
Who am I? Like everyone, I am the sum of my experiences.
Whenever I speak of "my" ideas or thoughts, what I really mean is the amalgamation of ideas I have picked up from others (and which I will do my best to explicitly reference when practical).

I wouldn't consider myself an expert in anything and neither have I made any meaningful contributions to human knowledge yet.
Take every post with a grain of salt.
I am simply trying to organize what I have gathered so far and put my opinions on paper.

{% for category in site.categories %}
  {% capture cat %}{{ category | first }}{% endcapture %}
  <h2 id="{{cat}}">{{ cat | capitalize }}</h2>
  {% for desc in site.descriptions %}
    {% if desc.cat == cat %}
      <p class="desc"><em>{{ desc.desc }}</em></p>
    {% endif %}
  {% endfor %}
  <ul class="posts-list">
  {% for post in site.categories[cat] %}
    <li>
      <strong>
        <a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
      </strong>
      <span class="post-date">- {{ post.date | date_to_long_string }}</span>
    </li>
  {% endfor %}
  </ul>
  {% if forloop.last == false %}<hr>{% endif %}
{% endfor %}
<br>
