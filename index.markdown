---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
pagination: 
  enabled: true
  per_page: 6
  permalink: '/page/:num/'
  title: ' Anime Now - Page :num'
  limit: 0
  sort_field: 'date'
  sort_reverse: true
---

{% for post in paginator.posts %}
{% assign truncated_content = post.content | strip_html | split: " " | slice: 0, 25 | join: " " | escape %}
{% assign bulan = "Jan,Feb,Maret,April,Mei,Juni,Juli,Ags,Sep,Okt,Nov,Des" | split: "," %}
{% assign bulan_angka = post.date | date: "%m" | minus: 1 %}
{% assign mm = bulan[bulan_angka] %}
<section class="post">
{% if post.image %}
<div class="post-thumb"><img src="/.netlify/images?url={{ post.image }}&fit=cover&w=92&h=92&fm=webp&q=75"></div>
{% endif %}
<div class="post-wrapper">
  <div class="post-meta">{{ post.author | default: site.author }} - {{ post.date | date: "%d" }} {{ mm }} {{ post.date | date: "%Y" }}</div>
  <h2 class="entry-title item-title"><a href="{{ post.url }}">{{ post.title }}</a></h2>
  <div class="entry-snippet">
    {% if post.description %}{{ post.description | escape }}{% else %}{{ truncated_content }}{% endif %}... <a class="readmore" href="{{ post.url }}">Selengkapnya&nbsp;»</a>
  </div>
</div>
</section>
{% endfor %}
