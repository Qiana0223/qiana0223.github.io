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
<h1 id="publications"></h1>

<h2 style="margin: 60px 0px -15px;">
Publications 

[comment]: <> (<temp style="font-size:15px;">[</temp><a href="https://scholar.google.com/citations?user=GJtATkAAAAAJ" target="_blank" style="font-size:15px;">Google Scholar</a><temp style="font-size:15px;">]</temp>)

</h2>

<!--<temp style="font-size:15px;">[</temp><a href="" target="_blank" style="font-size:15px;">DBLP</a><temp style="font-size:15px;">]</temp> -->

<div class="publications">
<ol class="bibliography">

[comment]: <> (--------for conference----------------------)

<h2 style="margin: 60px 0px -15px;">
Conference
</h2><br>

{% for link in site.data.publications.conference %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=50%">
            {% if link.conference_short %} 
            <abbr class="badge">{{ link.conference_short }}</abbr>
            {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.poster %} 
      <a href="{{ link.poster }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">poster</a>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>

<br>

{% endfor %}


[comment]: <> ([comment]: <> &#40;--------for workshop----------------------&#41;)

[comment]: <> (<h2 style="margin: 60px 0px -15px;">)

[comment]: <> (Workshop)

[comment]: <> (</h2><br>)

[comment]: <> ({% for link in site.data.publications.workshop %})

[comment]: <> (<li>)

[comment]: <> (<div class="pub-row">)

[comment]: <> (  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">)

[comment]: <> (    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">)

[comment]: <> (            {% if link.conference_short %} )

[comment]: <> (            <abbr class="badge">{{ link.conference_short }}</abbr>)

[comment]: <> (            {% endif %})

[comment]: <> (  </div>)

[comment]: <> (  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">)

[comment]: <> (      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>)

[comment]: <> (      <div class="author">{{ link.authors }}</div>)

[comment]: <> (      <div class="periodical"><em>{{ link.conference }}</em>)

[comment]: <> (      </div>)

[comment]: <> (    <div class="links">)

[comment]: <> (      {% if link.pdf %} )

[comment]: <> (      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>)

[comment]: <> (      {% endif %})

[comment]: <> (      {% if link.code %} )

[comment]: <> (      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>)

[comment]: <> (      {% endif %})

[comment]: <> (      {% if link.page %} )

[comment]: <> (      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>)

[comment]: <> (      {% endif %})

[comment]: <> (      {% if link.bibtex %} )

[comment]: <> (      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>)

[comment]: <> (      {% endif %})

[comment]: <> (      {% if link.notes %} )

[comment]: <> (      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>)

[comment]: <> (      {% endif %})

[comment]: <> (      {% if link.others %} )

[comment]: <> (      {{ link.others }})

[comment]: <> (      {% endif %})

[comment]: <> (    </div>)

[comment]: <> (  </div>)

[comment]: <> (</div>)

[comment]: <> (</li>)

[comment]: <> (<br>)

[comment]: <> ({% endfor %})

[comment]: <> (--------for journal----------------------)

<h2 style="margin: 60px 0px -15px;">
Journal
</h2><br>

{% for link in site.data.publications.journal %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
            {% if link.conference_short %} 
            <abbr class="badge">{{ link.conference_short }}</abbr>
            {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.poster %} 
      <a href="{{ link.poster }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">poster</a>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>

<br>

{% endfor %}

</ol>
</div>


