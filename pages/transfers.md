---
layout: best-practices
permalink: /best-practices/transfers/

table_data:
  transfers.transfer_type:
    1: "<q>0 or (empty): This is a recommended transfer point between routes.</q>
    If there are multiple transfer opportunities that include a superior option (i.e. a transit center with additional amenities or a station with adjacent or connected boarding facilities/platforms), specify a recommended transfer point.<!-- (50) -->"
    2: "<q>1: This is a timed transfer point between two routes. The departing vehicle is expected to wait for the arriving one,   with sufficient time for a passenger to transfer between routes.</q>
    This transfer type overrides a required interval to reliably make transfers.  As an example, Google Maps assumes that passengers need 3 minutes to safely make a transfer. Other applications may assume other defaults. <!-- (51) -->"
    3: "<q>2: This transfer requires a minimum amount of time between arrival and departure to ensure a connection. The time required to transfer is specified by <code>min_transfer_time</code>.</q>
    Specify minimum transfer time if there are obstructions or other factors which increase the time to travel between stops. <!-- (52) -->"
    4: "<q>3: Transfers are not possible between routes at this location.</q>
    Specify this value if transfers are not possible because of physical barriers, or if they are made unsafe or complicated by difficult road crossings or gaps in the pedestrian network. <!-- (53) -->"
    5: "If in-seat (block) transfers are allowed between trips, then the last stop of the arriving trip must be the same as the first stop of the departing trip. <!-- (55) -->"
---

## transfers.txt

`transfers.transfer_type` can be one of four values [defined in the GTFS](https://developers.google.com/transit/gtfs/reference/transfers-file). These `transfer_type` definitions are quoted from the GTFS Specification below, _in italics_, with additional practice recommendations. <!-- (49) -->

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
        <tr id="transfers_{{ recommendation[0] }}" class="anchor-row">
          <td>{% if forloop.first == true %}<code>{{ field_name[0] }}</code>{% endif %}</td>
          <td>{{ recommendation[0] }}</td>
          <td>{{ recommendation[1] }}</td>
        </tr>
      {% endfor %}
    {% endfor %}
  </tbody>
</table>
