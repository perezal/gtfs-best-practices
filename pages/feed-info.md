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
      <th>#</th>
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

<h3 id="feed-info">feed_info.txt</h3>


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
    <tr id="feed_info_1" class="anchor-row">
      <td><code>feed_publisher_name</code></td> <!-- (21) -->
      <td></td>
      <td>1</td>
      <td>Should be included</td>
    </tr>
    <tr id="feed_info_2" class="anchor-row">
      <td><code>feed_publisher_url</code></td> <!-- (22) -->
      <td></td>
      <td>2</td>
      <td>Should be included</td>
    </tr>
    <tr id="feed_info_3" class="anchor-row">
      <td><code>feed_lang</code></td> <!-- (23) -->
      <td></td>
      <td>3</td>
      <td>Should be included</td>
    </tr>
    <tr id="feed_info_4" class="anchor-row">
      <td><code>feed_start_date</code> & <code>feed_end_date</code></td> <!-- (24) -->
      <td></td>
      <td>4</td>
      <td>Should be included</td>
    </tr>
    <tr id="feed_info_5" class="anchor-row">
      <td><code>feed_version</code></td> <!-- (25) -->
      <td></td>
      <td>5</td>
      <td>Should be included</td>
    </tr>
    <tr id="feed_info_6" class="anchor-row">
      <td><code>feed_contact_email</code> & <code>feed_contact_url</code></td> <!-- (26) -->
      <td></td>
      <td>6</td>
      <td>Provide at least one</td>
    </tr>
  </tbody>
</table>
