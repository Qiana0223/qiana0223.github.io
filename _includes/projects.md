<!-- adapted from news.md and publications.md -->

<style>
    /* 样式定义 */
    .popup {
        display: none;
        position: fixed;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        padding: 20px;
        background-color: white;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
        z-index: 1000;
    }
    .popup .close {
        display: block;
        text-align: right;
        cursor: pointer;
    }
    #overlay {
        display: none;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        z-index: 999;
    }
</style>
<h1 id="projects"></h1>

<h2 style="margin: 60px 0px -50px;">Projects</h2>

<div class="projects">
<ol class="bibliography">

<h2 style="margin: 60px 0px -15px;">
Active Projects
</h2><br>

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
      <div class="title">{{ proj.title }}</div>
      <div class="proj_description">{{ proj.description }} </div>
    <div class="links">
      {% if proj.paper %} 
      <a href="{{ proj.paper }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">paper</a>
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

</ol>
</div>


<!-- old projects -->

<p> <a href="javascript:toggle_vis('newsmore')">Show more</a> </p>
<div id="newsmore" style="display:none">
<div class="projects">
<ol class="bibliography">
<h2 style="margin: 60px 0px -15px;">
Inactive Projects
</h2><br>
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
      <div class="title">{{ proj.title }}</div>
      <div class="proj_description">{{ proj.description }} </div>
    <div class="links">
      {% if proj.paper %} 
      <a href="{{ proj.paper }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">paper</a>
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

</ol>
</div>
</div>



