---
layout: best-practices
permalink: /best-practices/

---

# GTFS Data Best Practices

## Introduction

These are recommended practices for describing public transportation services in the [General Transit Feed Specification (GTFS)](https://gtfs.org). These practices have been synthesized from the experience of the [GTFS Best Practices working group](#working-group) members and [application-specific GTFS practice recommendations](http://www.transitwiki.org/TransitWiki/index.php/Best_practices_for_creating_GTFS). For further background, see the [Frequently Asked Questions](faq).

### Linking to This Document

Please link here in order to provide feed producers with guidance for correct formation of GTFS data. Each individual recommendation has an anchor link. Click the recommendation to get the URL for the in-page anchor link.

If a GTFS-consuming application makes requirements or recommendations for GTFS data practices that are not described here, it is recommended to publish a document with those requirements or recommendations to supplement these common best practices.

### Document Structure

Recommended practices are organized into three primary sections

* __[Dataset Publishing & General Practices](#publishing):__ These practices relate to the overall structure of the GTFS dataset and to the manner in which GTFS datasets are published.
* __[Practice Recommendations Organized by File](#by-file):__ Recommendations are organized by file and field in the GTFS to facilitate mapping practices back to the official GTFS reference.
* __[Practice Recommendations Organized by Case](#by-case):__ With particular cases, such as loop routes, practices may need to be applied across several files and fields. Such recommendations are consolidated in this section.

### System Tags

Five different tags are included throughout the list of practices. These tags indicate the type of systems that require the practice being described.

<span class="tag trip-planners"></span>

These practices improve customer experience in applications like Google Maps that are used for trip planning.

<span class="tag human-readability"></span>

These practices help maintain the ability for a human reader to unzip and examine GTFS files.

<span class="tag arrival-predictions"></span>

These practices allow arrival prediction software to create real-time arrival estimates related to the schedules in [`trips.txt`](/best-practices/trips) and [`stop_times.txt`](/best-practices/stop-times).

<span class="tag timetables"></span>

These practices support the creation of HTML timetables based on GTFS, such as with the GTFS-to-HTML software.

## About This Document

### Objectives

The objectives of maintaining GTFS Best Practices is to:

* Improve end-user customer experience in public transportation apps
* Make it easier for software developers to deploy and scale applications, products, and services
* Facilitate the use of GTFS in various application categories (beyond its original focus on trip planning)

### How to propose or amend published GTFS Best Practices

GTFS applications and practice evolve, and so this document may need to be amended from time to time. To propose an amendment to this document, open a pull request [in the GTFS Best Practices GitHub repository](https://github.com/rocky-mountain-institute/gtfs-best-practices) and advocate for the change. The GTFS Best Practices Working Group will meet quarterly to discuss and approve selected changes. Please send other questions or suggestions to [gtfs@rmi.org](mailto:gtfs@rmi.org).

## GTFS Best Practices Working Group

The GTFS Best Practices Working Group consists of public transportation providers, developers of GTFS-consuming applications, consultants, and academic organizations to define common practices and expectations for GTFS data. The goals of this working group are to support greater interoperability of data data. To join the working group, email [gtfs@rmi.org](mailto:gtfs@rmi.org).

Members of this working group include:

* [Apple](http://www.apple.com/)
* [Cambridge Systematics](https://www.camsys.com/)
* [Capital Metro](https://www.capmetro.org/)
* [Center for Urban Transportation Research at University of South Florida](https://www.cutr.usf.edu/)
* [Conveyal](http://conveyal.com/)
* [Google](https://www.google.com/)
* [IBI Group](http://www.ibigroup.com/)
* [Mapzen](https://mapzen.com/)
* [Microsoft](https://www.microsoft.com/)
* [Moovel](https://www.moovel.com/)
* [Oregon Department of Transportation](http://www.oregon.gov/odot/)
* [Swiftly](https://goswift.ly/)
* [Transit](https://transitapp.com/)
* [Trillium](http://trilliumtransit.com/)
* [TriMet](https://trimet.org/)
* [World Bank](http://www.worldbank.org/)

<figure>
  <a href="http://www.rmi.org/mobility" style="background-color: initial;"><img id="rmi-logo" src="/best-practices/images/rmi-small.png" alt="The Rocky Mountain Institute Mobility Transformation" width="240" height="63" border="0" style="height:63px;width:240px;"></a>
  <figcaption>The GTFS Best Practices Working Group is convened and facilitated by <a href="http://rmi.org/ITD">Rocky Mountain Institute</a> (RMI),an independent nonprofit founded in 1982. RMI is working to transform global energy use to create a clean, prosperous, and secure low-carbon future. It engages businesses, communities, institutions, and entrepreneurs to accelerate the adoption of market-based solutions that cost-effectively shift from fossil fuels to efficiency and renewables. RMI has offices in Basalt and Boulder, Colorado; New York City; Washington, D.C.; and Beijing.</figcaption>
</figure>
