<div class="grid-container-team">
  {% for supporter in include.supporters %}
      <div class="grid-child">
        {% if supporter.image %}
          <img alt="{{supporter.name}}" class="card-img img-thumbnail" src="{{ site.baseurl }}/assets/supporters/{{supporter.image}}" style="max-height: 10rem; width: auto;"><br>
        {% endif %}
        <a href="{{supporter.website}}"><b>{{supporter.name}}</b></a><br>
      </div>
  {% endfor %} 
</div>