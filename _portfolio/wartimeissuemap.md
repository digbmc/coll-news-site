---
title: Place Names in Wartime Issues # title for the visulization
layout: project
author: Avery Matteo 
auth_year: "'22"  
subtitle: Locations mentioned in wartime issues of the *College News* corpus
alt: A map documenting locations mentioned in wartime issues of the College News corpus

caption: # info that appears on homepage
  title: Place Names in Wartime Issues
  subtitle: Interactive map
  thumbnail: assets/img/portfolio/map-war.png # screenshot for your visualization. 
  alt: Locations mentioned in wartime issues of the College News corpus
---
Visitors can add or remove map layers by selecting the checkboxes in the panel to the left. Clicking on the map's pins will reveal the newspaper issue the location is in and its number of appearances in the issue.

<div style="text-align: center">
<iframe src="https://www.google.com/maps/d/u/0/embed?mid=1Ep4CjIcVGGvyQXFljUXzaUUpYhjsi-iI" width="640" height="480"></iframe>
</div>

My interest in Bryn Mawr students' geopolitical awareness began while exploring *College News* issues written during World War I. I noticed that the tone and scope of focus were quite different from issues published during carefree, campus-oriented periods of peace, and decided to embark on a more expansive mapping project that depicts international place names in issues published during World War I (1914-1918), World War II (1939-1945), the Korean War (1950-1953) and the Vietnam War up to 1968. I was only able to track the Vietnam War until 1968 because *The College News* was dissolved to form the *Bi-College News*, marking the conclusion of our corpus.

To bring this visualization to life, I used my team member Marianela's [spaCy Named Entity Recognition (NER) code](https://github.com/digbmc/college-news/blob/main/text-mining/cn-gpe-search.py) for Geopolitical Entity (GPE) extraction. She also created a cleaned version of the CSV file that was produced — filtering the results to omit non-place names and unrecognizable words — that I used for my map visualization. Next, I separated this whole-corpus CSV file into chunks encompassing the years associated with each war. I then uploaded these files as individual layers on [Google MyMaps](https://www.google.com/maps/about/mymaps/) so that website visitors have the ability to add or remove layers that represent each wartime period.

While my intention is to leave this map up for individual interpretation, the College News wartime issues seem to reveal that Bryn Mawr's student body was largely comprised of engaged global citizens who delegated attention not only to pressing campus issues, but also to salient political concerns that reached beyond the scope of the College.
