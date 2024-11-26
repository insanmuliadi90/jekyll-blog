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
<section class="post">
<div>{{ post.date | date: "%B %d, %Y" }}</div>
  <h2><a href="{{ post.url }}">{{ post.title }}</a></h2>
</section>
{% endfor %}
