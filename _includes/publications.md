<h2 id="publications" style="margin: 2px 0px 0px;">Publications</h2>

<p style="margin: 2px 0px -25px;">(Co-first author*, corresponding author†)</p>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

{% if link.image %}
<li>
{% else %}
<li style="height: 120px;">
{% endif %}
{% if link.image %}
<div class="pub-row">
{% else %}
<div class="pub-row" style="height: 120px;">
{% endif %}
  {% if link.image %} 
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 5px;">
  {% else %}
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 0px;padding-left: 0px;">
  {% endif %}
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% endif %}
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 5px;">
      <div class="title"><a href="{{ link.url }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical">{{ link.journal }} <strong>{{ link.volume }}</strong>{% if link.pages %},{% endif %} {{ link.pages }}  ({{ link.year }})
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
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>

{% endfor %}

</ol>
</div>

