---
layout: best-practices
permalink: /best-practices/agency/

table_data:
  agency_id:
    1: "Should be included, even if there is only one agency in the feed. (See also: recommendation to include <code>agency_id</code> in <a href='/best-practices/routes/'><code>routes.txt</code></a> and <a href='/best-practices/fare-attributes/'><code>fare_attributes.txt</code></a>)"
  agency_lang:
    2: "Should be included."
  agency_phone:
    3: "Should be included unless no such customer service phone exists."
  agency_email:
    4: "Should be included unless no such customer service email exists."
  agency_fare_url:
    5: "Should be included unless the agency is fully fare-free."
---

## agency.txt

<span class="tag trip-planners"></span>
<span class="tag human-readability"></span>
<span class="tag timetables"></span>

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
        <tr id="agency_{{ recommendation[0] }}" class="anchor-row">
          <td>{% if forloop.first %}<code>{{ field_name[0] }}</code>{% endif %}</td>
          <td class="anchor"><a href="#agency_{{ recommendation[0] }}">{{ recommendation[0] }}</a></td>
          <td>{{ recommendation[1] }}</td>
        </tr>
      {% endfor %}
    {% endfor %}
  </tbody>
</table>

<table class="recommendation">
  <thead>
    <tr>
      <th>Field Name</th>
      <th>Tags</th>
      <th>#</th>
      <th>Recommendation</th>
    </tr>
  </thead>
  <tbody>
    <tr id="agency_1" class="anchor-row">
      <td><code>agency_id</code></td> <!-- (15) -->
      <td></td>
      <td>1</td>
      <td>Should be included, even if there is only one agency in the feed. (See also: recommendation to include <code>agency_id</code> in <a href="#routes"><code>routes.txt</code></a> and <a href="#fare-rules"><code>fare_attributes.txt</code></a>)</td>
    </tr>
    <tr id="agency_2" class="anchor-row">
      <td><code>agency_lang</code></td> <!-- (16) -->
      <td></td>
      <td>2</td>
      <td>Should be included</td>
    </tr>
    <tr id="agency_3" class="anchor-row">
      <td><code>agency_phone</code></td> <!-- (17) -->
      <td></td>
      <td>3</td>
      <td>Should be included unless no such customer service phone exists.</td>
    </tr>
    <tr id="agency_4" class="anchor-row">
      <td><code>agency_email</code></td> <!-- (18) -->
      <td></td>
      <td>4</td>
      <td>Should be included unless no such customer service email exists.</td>
    </tr>
    <tr id="agency_5" class="anchor-row">
      <td><code>agency_fare_url</code></td> <!-- (19) -->
      <td></td>
      <td>5</td>
      <td>Should be included unless the agency is fully fare-free.</td>
    </tr>
  </tbody>
</table>
