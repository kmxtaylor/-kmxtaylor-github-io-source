---
title: "Address Lookup Widgets"
leftImgSrc: "/img/census-narrative-profiles-mobile.png"
leftImgAlt: "Results of searching SPIE's address: 'Census Tract 11.01' & its narrative profile link."
weight: 2
# type: "portfolio"
# layout: "project"
draft: false
---

I developed a widget to make Census neighborhood data more easily accessible toward the end of my Software Engineering Fellowship at the Census Bureau. The problem I was looking to solve was that when users wanted to see data for their neighborhood, they had to approximate that area with their Census Tract, but tracts have unintuitive names like “Census Tract 401.03” and can be tricky to figure out.

I took ownership of the project to create a scalable Census address lookup widget where a user could enter an address and get back its geography labels — with the goal of it being added in various places around Census.gov with a similar need. Similar to the other projects during my Fellowship at the Census, I created the tool using JavaScript, HTML and CSS with Bootstrap and jQuery.

To make the widget as adaptable for the Census Bureau’s needs as possible, I created multiple versions of the widget:

1. The main version that fetches the most common geography labels
2. A simplified version of the widget for a single geography: Census tracts for looking up neighborhood data (the original use case)
3. An extended version of the widget that also links to narrative profiles for the geographies on the Census Narrative Profiles app

The Census Bureau ultimately added the extended version of my widget to the Census Narrative Profiles web app and may use it in other parts of the site in the future.

Check out the widget in-action in the [live Census Narrative Profiles Tool](https://www.census.gov/acs/www/data/data-tables-and-tools/narrative-profiles/) (under “Use Address Lookup”), the [source code](https://github.com/kmxtaylor/address-lookup-widget) and our [presentation slides with more info](https://docs.google.com/presentation/d/1DdZueQ0q6X1-RabHOYPNUKv0fdWU-Hvc4-ss1xGjmQ4/edit?usp=drive_link)!
