---
title: South Asian Keywords  
layout: project
# author of the visualization along with the class year 
author: Aanandi Murlidharan
auth_year: "'23"
image:  # if using image for viz

caption: # info that appears on homepage
  title: South Asian Keywords
  subtitle:
  thumbnail: assets/img/portfolio/southasiavisualization.png
  alt: map placeholder image
---
<div id="vis"></div>

<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega@5"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-lite@4.8.1"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-embed@6"></script>
  <script>
    (function(vegaEmbed) {
      var embedOpt = {"mode": "vega-lite"};

      function showError(el, error){
          el.innerHTML = ('<div class="error" style="color:red;">'
                          + '<p>JavaScript Error: ' + error.message + '</p>'
                          + "<p>This usually means there's a typo in your chart specification. "
                          + "See the javascript console for the full traceback.</p>"
                          + '</div>');
          throw error;
      }
      const el = document.getElementById('vis');
      vegaEmbed("#vis", spec, embedOpt)
        .catch(error => showError(el, error));
    })(vegaEmbed);

  </script> 
<!--  
insert visualization code or embedding here
If using an image file for viz, use image variable in header
--> 

This project originally began with an intention to highlight the voices of South Asian Students in Bryn Mawr College. However, upon developing this project, I discovered that there were little to no mentions of the stories of South Asian Bryn Mawr students. Rather it was mostly mention to the current events of south Asia. Therefore, I decided to present the data of two countries in South Asia (India and Pakistan) and the two largest religious groups in South Asia (Hindus and Muslims). 


The data for the visualization was retrieved through a multiple keyword context search code. Using this code, I was able to pull every mention of the words “india, Pakistan, and Hindu” along with a 200 character context to each mention from the corpus by issue date and year. I then used Altair to create my final data visualization.  I used the strip plot graph within the Altair library and added tool tips to include the context behind the mention of the specific word in the context.  Finally, I used the converted it to an HTML and uploaded it to the site.


