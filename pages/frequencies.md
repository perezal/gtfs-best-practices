---
layout: best-practices
permalink: /best-practices/frequencies/

table_data:
  1: "Actual stop times are ignored for trips referenced by <code>frequencies.txt</code>; only travel time intervals between stops are significant for frequency-based trips. For clarity/human readability, it is recommended that the first stop time of a trip referenced in <code>frequencies.txt</code> should begin at 00:00:00 (first <code>arrival_time</code> value of 00:00:00). <!-- (99) -->"
  2: "<code>block_id</code> can be provided for frequency-based trips. <!-- (101) -->"
---

## frequencies.txt

<table class="recommendation">
  <thead>
    <tr>
      <th>ID</th>
      <th>Recommendation</th>
    </tr>
  </thead>
  <tbody>
    {% for recommendation in page.table_data %}
      <tr id="fare_rules_{{ recommendation[0] }}" class="anchor-row">
        <td>{{ recommendation[0] }}</td>
        <td>{{ recommendation[1] }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>
