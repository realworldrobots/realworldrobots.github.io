<div class="grid-container-team">
  {% for person in include.people %}
      <div class="grid-child">
        <img alt="{{person.name}}" class="card-img img-thumbnail" src="{{ site.baseurl }}/assets/people/{{person.image}}" style="max-height: 10rem; width: auto;"><br>
        <b>{{person.name}}</b><br>
        {{person.title}}<br>
        <i>{{person.affiliation}}</i><br>
        <a href="{{person.website}}">Personal Website</a><br>
      </div>
  {% endfor %} 
</div>

