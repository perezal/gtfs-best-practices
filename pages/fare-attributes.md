---
layout: best-practices
permalink: /best-practices/fare-attributes/

table_data:
  1: "<code>agency_id</code> should be included in <code>fare_attributes.txt</code> if it the field is included in <code>agency.txt</code>. <!-- (84) -->"
  2: "If a fare system cannot be accurately modeled, avoid further confusion and leave it blank. <!-- (85) -->"
  3: "Include fares (<code>fare_attributes.txt</code> and <code>fare_rules.txt</code>) and model them as accurately as possible. In edge cases where fares cannot be accurately modeled, the fare should be represented as more expensive rather than less expensive so customers will not attempt to board with insufficient fare. If the vast majority of fares cannot be modeled correctly, do not include fare information in the feed. <!-- (86) -->"

---

## fare_attributes.txt

<table class="recommendation">
  <thead>
    <tr>
      <th>ID</th>
      <th>Recommendation</th>
    </tr>
  </thead>
  <tbody>
    {% for recommendation in page.table_data %}
      <tr id="fare_attributes_{{ recommendation[0] }}" class="anchor-row">
        <td>{{ recommendation[0] }}</td>
        <td>{{ recommendation[1] }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>
