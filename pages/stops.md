---
layout: best-practices
permalink: /best-practices/stops/

table_data:
  stop_id:
    1: "Stops that are in different physical locations (i.e., different designated precise locations for vehicles on designated routes to stop, potentially distinguished by signs, shelters, or other such public information, located on different street corners or representing different boarding facility such as a platform or bus bay, even if nearby each other) should have different <code>stop_id</code>. <!-- (27) -->"
    2: "<code>stop_id</code> is an internal ID, not intended to be shown to passengers. <!-- (38) -->"
    3: "Maintain consistent <code>stop_id</code> for the same stops across data iterations (see: <a href='/best-practices/publishing'>Dataset Publishing & General Practices</a>). <!-- (28) -->"
  stop_name:
    4: "The <code>stop_name</code> should match the agency's public name for the stop, station, or boarding facility, e.g. what is printed on a timetable, published online, and/or presented at the location. <!-- (29) -->"
    5: "When there is not a published stop name, follow consistent stop naming conventions throughout the feed. <!-- (30) -->"
    6: "Avoid use of abbreviations other than for places that are most commonly called by an abbreviated name. See Abbreviations (#2) under <a href='/best-practices/all-files'>All Files</a>. <!-- (31) -->"
    7: "Provide stop names in mixed case, following local conventions, as per recommendation for all customer-facing text fields. <!-- (32) -->"
    8: "By default, <code>stop_name</code> should not contain generic or redundant words like “Station” or “Stop”, but some edge cases are allowed:
      <ul>
        <li>When it is actually part of the name (Union Station, Central Station)</li>
        <li>When the <code>stop_name</code> is too generic (such as if it is the name of the city). “Station”, “Terminal”, or other words make the meaning clear.</li>
      </ul>"
  stop_lat:
    9: "Stop locations should be as accurate possible. Stop locations should have an error of <strong>no more</strong> than four meters when compared to the actual stop position.<!-- (34) -->"
    10: "Stop locations should be placed very near to the pedestrian right of way where a passenger will board (i.e. correct side of the street).<!-- (35) -->"
    11: "If a stop location is shared across separate data feeds (i.e. two agencies use exactly the same stop / boarding facility), indicate the stop is shared by using the exact same <code>stop_lat</code> and <code>stop_lon</code> for both stops.<!-- (36) -->"
  stop_lon:
    15: "See recommendations for <code>stop_lat</code> (above)"
  stop_code:
    12: "<code>stop_code</code> should be included in GTFS if there are passenger-facing stop numbers or short identifiers.<!-- (37) -->"
  parent_station:
    13: "Many stations or terminals have multiple boarding facilities (depending on mode, they might be called a bus bay, platform, wharf, gate, or another term). In such cases, feed producers should describe stations, boarding facilities (also called child stops), and their relation. <!-- (40) -->
    <ul>
      <li>The station or terminal should be defined as a record in <code>stops.txt</code> with <code>location_type = 1</code>.</li>
      <li>Each boarding facility should be defined as a stop with <code>location_type = 0</code>. The <code>parent_station</code> field should reference the <code>stop_id</code> of the station the boarding facility is in.</li>
    </ul>"
    14: "When naming the station and child stops, set names that are well-recognized by riders, and can help riders to identify the station and boarding facility (bus bay, platform, wharf, gate, etc.). <!-- (41) -->
      <table class='example'>
        <thead>
          <tr>
            <th>Parent Station Name</th>
            <th>Child Stop Name</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>
            <a href='/best-practices/images/chicago-union'>Chicago Union Station</a>
            </td>
            <td>Chicago Union Station Platform 19</td>
          </tr>
          <tr>
            <td><a href='/best-practices/images/sf-ferry'>San Francisco Ferry Building Terminal</a></td>
            <td>San Francisco Ferry Building Terminal Gate E</td>
          </tr>
          <tr>
            <td><a href='/best-practices/images/transit-center'>Downtown Transit Center</a></td>
            <td>Downtown Transit Center Bay B</td>
          </tr>
        </tbody>
      </table>"
  location_type:
    16: "See recommendations for <code><a href='#stops_13'>parent_station</a></code> (above)"
---

## stops.txt

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
        <tr id="stops_{{ recommendation[0] }}" class="anchor-row">
          <td>{% if forloop.first == true %}<code>{{ field_name[0] }}</code>{% endif %}</td>
          <td>{{ recommendation[0] }}</td>
          <td>{{ recommendation[1] }}</td>
        </tr>
      {% endfor %}
    {% endfor %}
  </tbody>
</table>
