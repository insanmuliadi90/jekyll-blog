---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
pagination: 
  enabled: true
  per_page: 6
  permalink: '/page/:num/'
  title: ' - page :num'
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
{% if post.images %}
<div class="post-thumb"><img src="{{ post.image }}"></div>
{% endif %}
<div class="post-meta">{{ post.date | date: "%d" }} {{ mm }} {{ post.date | date: "%Y" }}</div>
  <h2 class="entry-title"><a href="{{ post.url }}">{{ post.title }}</a></h2>
  {% if post.description %}{{ post.description | escape }}{% else %}{{ truncated_content }}{% endif %}... <a href="{{ post.url }}">Selengkapnya</a>
  
</section>
{% endfor %}
