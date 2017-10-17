---
layout: best-practices
permalink: /best-practices/calendar/

table_data:
  1: "<code>calendar_dates.txt</code> should only contain a limited number of exceptions to the schedule. Regularly-scheduled service should be configured using <code>calendar.txt</code>."
  2: "Including a <code>calendar.service_name</code> field can also increase the human readability of GTFS, although this is not adopted in the spec."

---

## calendar.txt

<table class="recommendation">
  <thead>
    <tr>
      <th>ID</th>
      <th>Recommendation</th>
    </tr>
  </thead>
  <tbody>
    {% for recommendation in page.table_data %}
      <tr id="calendar_{{ recommendation[0] }}" class="anchor-row">
        <td>{{ recommendation[0] }}</td>
        <td>{{ recommendation[1] }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>

<h3 id="calendar">calendar.txt and calendar_dates.txt</h3>

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
    <tr id="calendar_1" class="anchor-row">
      <td rowspan="2"><code></code></td>
      <td>
        <span class="tag human-readability"></span>
        <span class="tag timetables"></span>
      </td>
      <td>1</td>
      <td><code>calendar_dates.txt</code> should only contain a limited number of exceptions to the schedule. Regularly-scheduled service should be configured using <code>calendar.txt</code>.</td>
    </tr>
    <tr id="calendar_2" class="anchor-row">
      <td></td>
      <td>2</td>
      <td>Including a <code>calendar.service_name</code> field can also increase the human readability of GTFS, although this is not adopted in the spec.</td>
    </tr>
  </tbody>
</table>
