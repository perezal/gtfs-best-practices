---
layout: best-practices
permalink: /best-practices/loop-routes/

table_data:
  trips.trip_id:
    1: "Model the complete round-trip for the loop with a single trip.  <!-- (102) -->"
  stop_times.stop_id:
    2: "Include the first/last stop twice in <code>stop_times.txt</code> for the trip that is a loop. Example below. <!-- (87) -->

      <table class='example'>
        <thead>
          <tr>
            <th><code>trip_id</code></th>
            <th><code>stop_id</code></th>
            <th><code>stop_sequence</code></th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>9000</td>
            <td>101</td>
            <td>1</td>
          </tr>
          <tr>
            <td>9000</td>
            <td>102</td>
            <td>2</td>
          </tr>
          <tr>
            <td>9000</td>
            <td>103</td>
            <td>3</td>
          </tr>
          <tr>
            <td>9000</td>
            <td>101</td>
            <td>4</td>
          </tr>
        </tbody>
      </table>

    Often, a loop route may include first and last trips that do not travel the entire loop. Include these trips as well."
  trips.direction_id:
    3: "If loop operates in opposite directions (i.e. clockwise and counterclockwise), then designate <code>direction_id</code> as <code>0</code> or <code>1</code>. <!-- (89) -->"
  trips.block_id:
    4: "Indicate continuous loop trips with the same <code>block_id</code>. <!-- (90) -->"
---

## Loop Routes

On loop routes, vehicles’ trips begin and end at the same location (sometimes a transit or transfer center). Vehicles usually operate continuously and allow passengers to stay onboard as the vehicle continues its loop.

<figure id="loop-route-fig">
  <figcaption>Below: Loop route. The vehicle returns to the starting point in one trip. Some loop routes offer travel in one direction, and others in two directions.</figcaption>
  <img src="{{ "/best-practices/images/loop-route.svg" | prepend: site.baseurl }}" alt="A Loop Route">
</figure>

<table class="recommendation">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>ID</th>
      <th>Recommendation</th>
    </tr>
  </thead>
  <tbody>
    {% for field_name in page.table_data %}
      {% for recommendation in field_name[1] %}
        <tr id="loop_route_{{ recommendation[0] }}" class="anchor-row">
          <td>{% if forloop.first %}<code>{{ field_name[0] }}</code>{% endif %}</td>
          <td>{{ recommendation[0] }}</td>
          <td>{{ recommendation[1] }}</td>
        </tr>
      {% endfor %}
    {% endfor %}
  </tbody>
</table>
