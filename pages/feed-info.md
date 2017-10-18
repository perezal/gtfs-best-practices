---
layout: best-practices
permalink: /best-practices/feed-info/

table_data:
  feed_publisher_name:
    1: "Should be included."
  feed_publisher_url:
    2: "Should be included."
  feed_lang:
    3: "Should be included."
  feed_start_date:
    4: "Should be included."
  feed_end_date:
    7: "Should be included."
  feed_version:
    5: "Should be included."
  feed_contact_email:
    6: "Should be included."
  feed_contact_url:
    8: "Should be included."
---

## feed_info.txt


<span class="tag trip-planners"></span>
<span class="tag human-readability"></span>

`feed_info.txt` should be included, with all fields below. <!-- (20) -->

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
        <tr id="feed_info_{{ recommendation[0] }}" class="anchor-row">
          <td>{% if forloop.first == true %}<code>{{ field_name[0] }}</code>{% endif %}</td>
          <td>{{ recommendation[0] }}</td>
          <td>{{ recommendation[1] }}</td>
        </tr>
      {% endfor %}
    {% endfor %}
  </tbody>
</table>
