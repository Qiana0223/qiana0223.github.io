<h1 id="services"></h1>

<h2 style="margin: 60px 0px 10px;">Services</h2>

<h3 style="margin:0 10px 0;">Conference</h3>
<ul style="margin:0 0 5px;">
{% for item in site.data.service.conference %}
  <li><a href="{{ item.link }}"><autocolor>{{ item.content }}</autocolor></a></li>
{% endfor %}
</ul>
