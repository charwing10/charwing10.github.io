---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
title: Home
---
### About me:

<p align="center">
  <img src="/assets/qiaoying.jpg" alt="Qiaoying" title="Photo" width="250">
  <br><br>
  <a href="charwinghuang@gmail.com">charwinghuang@gmail.com</a> |
  <a href="https://github.com/charwing10">Github</a> |
  <a href="https://scholar.google.com/citations?hl=en&user=6u-go5UAAAAJ&view_op=list_works">Google Scholar</a>
</p>

I'm a Ph.D. student from Rutgers University. My advisor is Dimitris Metaxas. Currently, my research focus on MRI reconstruction, cardiac image segmentation, cardiac 3D modeling and etc..

{% for post in site.posts %}
      {% if post.title != null %}
        <div class="tagged-post">
          <h3 class="title">
            <a href="{{ post.url | relative_url }}">
              {{ post.title }}
            </a>
          </h3>
          {% if post.feature_img %}
              {% include post-featured-image.html image=post.featured-image alt=post.featured-image-alt %}
          {% endif %}
          <div class="meta">
            {{ post.date | date: "%B %-d, %Y" }}
          </div>
        </div>
      {% endif %}
{% endfor %}
