---
layout: best-practices
permalink: /best-practices/branches/

table_data:
  1: "In naming branch routes, it is recommended to follow other passenger information materials. Below are descriptions and examples of two cases: <!-- (97) -->"
  1A: "If timetables and on-street signage represent two distinctly named routes (e.g. 1A and 1B), then present this as such in the GTFS, using the <code>route_short_name</code> and/or <code>route_long_name</code> fields. <!-- (97A) -->
  Example: <a href='/best-practices/branch-example-godurham/'>GoDurham Transit routes 2, 2A, and 2B</a> demonstrate branched routes with deviations and extensions."
  1B: "If agency-provided information describes branches as the same named route, then utilize the <code>trips.trip_headsign</code>, <code>stop_times.stop_headsign</code>, and/or <code>trips.trip_short_name</code> fields. <!-- (97B) -->
  Example: GoTriangle <a href='http://admin.gotransitnc.org/sites/default/files/maps-and-schedules/gotriangle/RoutesAndSchedules-1561.pdf'>route 300</a> travels to different locations depending on the time of day. During peak commuter hours extra legs are added onto the standard route to accommodate workers entering and leaving the city."


---

## Branches

Some routes may include branches. Alignment and stops are shared amongst these branches, but each also serves distinct stops and alignment sections. The relationship among branches may be indicated by route name(s), headsigns, and trip short name using the further guidelines below.

<figure id="branching-fig">
<figcaption>Below: Three potential configurations of route branches. Primary alignment is in black. Branch is colored gold.</figcaption>
  <img src="{{ "/best-practices/images/branching.svg" | prepend: site.baseurl }}" alt="Configurations of Route Branches">
</figure>

<table class="recommendation">
  <thead>
    <tr>
      <th>ID</th>
      <th>Recommendation</th>
    </tr>
  </thead>
  <tbody>
    {% for recommendation in page.table_data %}
      <tr id="branches_{{ recommendation[0] }}" class="anchor-row">
        <td>{{ recommendation[0] }}</td>
        <td>{{ recommendation[1] }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>
