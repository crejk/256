{% include newsletter-input.md %}

{% include episodes-list.md %}

# Tags

{% assign tags = site.tags | sort %}
{% for tag in tags %}
  <h2>{{ tag[0] }}</h2>
  <ul>
    {% for post in tag[1] %}
      <li><a href="{{ post.url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
{% endfor %}