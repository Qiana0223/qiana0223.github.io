<!-- adapted from news.md -->

<h1 id="news"></h1>

<h2 style="margin: 60px 0px 10px;">Projects</h2>

<ul>
<!-- current projects -->
{% for proj in site.data.projects.current %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ proj.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
            {% if proj.project_short %} 
            <abbr class="badge">{{ proj.project_short }}</abbr>
            {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">      
      <div class="proj_description"><em>{{ proj.description }}</em> </div>
    <div class="links">
      {% if proj.pdf %} 
      <a href="{{ proj.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if proj.code %} 
      <a href="{{ proj.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if proj.page %} 
      <a href="{{ proj.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
    </div>
  </div>
</div>
</li>

<br>

{% endfor %}



<!-- old projects -->
<li> <a href="javascript:toggle_vis('newsmore')">Show more</a> </li>
<div id="newsmore" style="display:none">

{% for proj in site.data.projects.old %}
<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ proj.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
            {% if proj.project_short %} 
            <abbr class="badge">{{ proj.project_short }}</abbr>
            {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">      
      <div class="proj_description"><em>{{ proj.description }}</em> </div>
    <div class="links">
      {% if proj.pdf %} 
      <a href="{{ proj.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if proj.code %} 
      <a href="{{ proj.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if proj.page %} 
      <a href="{{ proj.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
    </div>
  </div>
</div>
</li>

<br>

{% endfor %}
</div>

</ul>
