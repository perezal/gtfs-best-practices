---
layout: best-practices
permalink: /best-practices/lasso-routes/

table_data:
  trips.trip_id:
    1: "The full extent of a 'vehicle round-trip' (see illustration <a href='#lasso-route-fig'>above</a>) consists of travel from A to B to B and back to A. An entire vehicle round-trip may be expressed by: <!-- (103) -->

      <ul>
        <li>A <strong>single</strong> <code>trip_id</code> value/record in <code>trips.txt</code></li>
        <li><strong>Multiple</strong> <code>trip_id</code> values/records in <code>trips.txt</code>, with continuous travel indicated by <code>block_id</code>.</li>
      </ul>"
  stop_times.stop_headsign:
    2: "The stops along the A-B section will be passed through in both directions. <code>stop_headsign</code> facilitates distinguishing travel direction. Therefore, providing <code>stop_headsign</code> is recommended for these trips. <!-- (94) -->

      <table class='example'>
        <thead>
          <tr>
            <th>Examples:</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>'A via B'</td>
          </tr>
          <tr>
            <td>'A'</td>
          </tr>
        </tbody>
      </table>

      <table class='example'>
        <thead>
          <tr>
            <th>Chicago Transit Authority's <a href='http://www.transitchicago.com/purpleline/'>Purple Line</a></th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>'Southbound to Loop'</td>
          </tr>
          <tr>
            <td>'Northbound via Loop'</td>
          </tr>
          <tr>
            <td>'Northbound to Linden'</td>
          </tr>
        </tbody>
      </table>

      <table class='example'>
        <thead>
          <tr>
            <th>Edmonton Transit Service Bus Lines, here <a href='http://webdocs.edmonton.ca/transit/route_schedules_and_maps/future/RT039.pdf'>the 39</a></th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>'Rutherford'</td>
          </tr>
          <tr>
            <td>'Century Park'</td>
          </tr>
        </tbody>
      </table>"
  trips.trip_headsign:
    3: "The trip headsign should be a global description of the trip, like displayed in the schedules. Could be “Linden to Linden via Loop” (Chicago example), or “A to A via B” (generic example). <!-- (95) -->"

---


## Lasso Routes

Lasso routes combine aspects of a loop route and directional route.

<figure id="lasso-route-fig">
  <figcaption style="max-width: 50%; display: inline-block;">Right - Lasso routes are loop-routes from A to A via B with three sections:<br>
    <ul>
      <li>straight section from A to B;</li>
      <li>loop from and to B;</li>
      <li>straight section from B to A.</li>
    </ul>
  </figcaption>
  <img style="max-width: 30%; display: inline-block;" src="{{ "/best-practices/images/lasso-route.svg" | prepend: site.baseurl }}" alt="A Lasso Route">
</figure>

<table class="example">
  <thead>
    <tr>
      <th>Examples:</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Subway Routes (<a href="http://www.transitchicago.com/assets/1/maps/L_Map_March_2016_s_lite.pdf">Chicago</a>)</td>
    </tr>
    <tr>
      <td>Bus Suburb to Downtown Routes (<a href="https://stalbert.ca/uploads/PDF-infosheets/201_207_Fall_2016.pdf">St. Albert</a> or <a href="http://webdocs.edmonton.ca/transit/route_schedules_and_maps/future/RT039.pdf">Edmonton</a>)</td>
    </tr>
    <tr>
      <td>See CTA Brown Line (<a href="http://www.transitchicago.com/brownline/">CTA Website</a> and <a href="https://transitfeeds.com/p/chicago-transit-authority/165/latest/route/Brn">TransitFeeds</a>)</td>
    </tr>
  </tbody>
</table>

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
        <tr id="lasso_route_{{ recommendation[0] }}" class="anchor-row">
          <td>{% if forloop.first == true %}<code>{{ field_name[0] }}</code>{% endif %}</td>
          <td>{{ recommendation[0] }}</td>
          <td>{{ recommendation[1] }}</td>
        </tr>
      {% endfor %}
    {% endfor %}
  </tbody>
</table>
