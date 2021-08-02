---
title: Place Names in Wartime Issues # title for the visulization
layout: project
author: Avery Matteo 
auth_year: "'22"  
subtitle: Locations mentioned in wartime issues of the College News corpus
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

My interest in Bryn Mawr students' geopolitical awareness began while exploring College News issues written during World War I. I noticed that the tone and scope of focus were quite different from issues published during more carefree, campus-oriented periods of peace — and decided to embark on a more expansive mapping project that depicts international place names in issues published during World War I, World War II, the Korean War and the Vietnam War up to 1968.

To bring this visualization to life, I used a [Named Entity Recognition (NER)](https://towardsdatascience.com/named-entity-recognition-with-nltk-and-spacy-8c4a7d88e7da) to identify geopolitical entities (GPEs). I then used the CSV file that was produced to build a [Google MyMaps](https://www.google.com/maps/about/mymaps/) visualization. 

While my intention is to leave this map up for individual interpretation, the College News wartime issues seem to reveal that Bryn Mawr's student body was largely comprised of engaged global citizens who delegated attention not only to pressing campus issues, but to salient political concerns that reached beyond the scope of the College as well.


