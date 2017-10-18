---
layout: best-practices
permalink: /best-practices/publishing/


table_data:
  1: "Datasets should be published at a public, permanent URL, including the zip file name. (e.g., <a href='http://www.agency.org/gtfs/gtfs.zip'>www.agency.org/gtfs/gtfs.zip</a>).  Ideally, the URL should be directly downloadable without requiring login to access the file, to facilitate download by consuming software applications.<!-- (1) --> While it is recommended (and the most common practice) to make a GTFS dataset openly downloadable, if a data provider does need to control access to GTFS for licensing or other reasons, it is recommended to control access to the GTFS dataset using API keys, which will facilitate automatic downloads. <!-- (2) -->"
  2: "GTFS data is published in iterations so that a single file at a stable location always contains the latest official description of service for a transit agency (or agencies). <!-- (3) -->"
  3: "Maintain persistent identifiers (id fields) for <code>stop_id</code>, <code>route_id</code>, and <code>agency_id</code> across data iterations whenever possible. <!-- (4) -->"
  4: "One GTFS dataset should contain current and upcoming service (sometimes called a “merged” dataset). Google transitfeed tool's <a href='https://github.com/google/transitfeed/wiki/Merge'>merge function</a> can be used to create a merged dataset from two different GTFS feeds. <!-- (5) -->

    <ul>
      <li>At any time, the published GTFS dataset should be valid for at least the next 7 days, and ideally for as long as the operator is confident that the schedule will continue to be operated.</li>
      <li>If possible, the GTFS dataset should cover at least the next 30 days of service.</li>
    </ul>"
  5: "Remove old services (expired calendars) from the feed. <!-- (10) -->"
  6: "If a service modification will go into effect in 7 days or fewer, express this service change through a <a href='https://developers.google.com/transit/gtfs-realtime/'>GTFS-realtime</a> feed (service advisories or trip updates) rather than static GTFS dataset. <!-- (8) -->"
  7: "The web-server hosting GTFS data should be configured to correctly report the file modification date (see <a href='https://tools.ietf.org/html/rfc2616#section-14.29'>HTTP/1.1 - Request for Comments 2616</a>, under Section 14.29). <!-- (9) -->"

---

## Dataset Publishing & General Practices

<table class="recommendation">
  <thead>
    <tr>
      <th>ID</th>
      <th>Recommendation</th>
    </tr>
  </thead>
  <tbody>
    {% for recommendation in page.table_data %}
      <tr id="publishing_{{ recommendation[0] }}" class="anchor-row">
        <td>{{ recommendation[0] }}</td>
        <td>{{ recommendation[1] }}</td>
      </tr>
    {% endfor %}
  </tbody>
</table>
