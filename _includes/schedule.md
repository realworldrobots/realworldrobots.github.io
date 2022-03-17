### Schedule

<div id = "LOCAL_TIME_SCHEDULE"></div>

<table>
  <thead>
    <tr>
      <th>Time</th>
      <th>Topic</th>
    </tr>
  </thead>
  <tbody>
    {% for event in include.schedule %}
    <tr>
      <td>{{event.time}}</td>
      <td>{{event.topic}}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>

<script>
  // top time
  var start = new Date('{{ site.data.settings.workshop_date_short }} {{ site.data.settings.start_time }} {{ site.data.settings.time_zone }}');
  var end = new Date('{{ site.data.settings.workshop_date_short }} {{ site.data.settings.end_time }} {{ site.data.settings.time_zone }}');
  var localTime = start.toLocaleTimeString([], {timeStyle: 'short'}) + " to " + end.toLocaleTimeString([], {timeStyle: 'short'});
  var startString = "The workshop will run from {{ site.data.settings.start_time }} to {{ site.data.settings.end_time }} {{ site.data.settings.time_zone_long }} which is "
  var endString = " in your local timezone (according to your computer system time)."
  document.getElementById('LOCAL_TIME_SCHEDULE').innerHTML = startString + localTime + endString;
  
  // all times
  var timeElements = document.getElementsByClassName("EDT_TIME");
  for (var i = 0; i < timeElements.length; i++) {
    dateStr = '{{ site.data.settings.workshop_date_short }} ' + timeElements[i].innerHTML + ' EDT'
    var gmt_time = new Date(dateStr);
    timeElements[i].innerHTML = gmt_time.toLocaleTimeString([], {timeStyle: 'short'})
  }
</script>