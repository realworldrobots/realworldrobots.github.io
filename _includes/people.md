### {{ include.title }}

<div class="grid-container-team">
  {% for person in include.people %}
      <div class="grid-child">
        {% if person.image %}
          <img alt="{{person.name}}" class="card-img img-thumbnail" src="{{ site.baseurl }}/assets/people/{{person.image}}" style="max-height: 10rem; width: auto;"><br>
        {% endif %}
        <b>{{person.name}}</b><br>
        {% if person.title %}{{person.title}}<br>{% endif %}
        <i>{{person.affiliation}}</i><br>
        {% if person.title2 And person.affiliation2 %}
        {{person.title2}}<br>
        <i>{{person.affiliation2}}</i><br>
        {% endif %}
        <a href="{{person.website}}">Personal Website</a><br>
      </div>
  {% endfor %} 
</div>

