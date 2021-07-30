---
title: Mentions of Cigarette and Smoking in The College News
layout: project
author: Al Nash
auth_year: "'23"
subtitle: Relative Frequency Visualized in a Bar Graph
alt: Individual Project
order: 3

caption: 
  title: Mentions of Cigarette and Smoking in The College News
  subtitle: Relative Frequency Visualized in a Bar Graph
  thumbnail: assets/img/portfolio/image.png
  alt: Individual Project
---

 <div id="vis"></div>


   I have always been interested in discovering trends and patterns within our volumious corpus, so at the initial stage of my individual project, I ran a few keyword searches through the whole corpus using python library [Regular Expression (RegEx)](https://docs.python.org/3/library/re.html). I chose to look into the frequency of the word "cigarette" mostly because of the abundance of tobacco ads in The College News. The keyword search of "cigarette" and "smoking" returned over 2800 results--a shockingly high number to my generation considering its nowadays well-known negative impact on health. After a casual discussion with a few members on the project team, I realized the frequency of smoking related terms might form a pattern that potentially correlates to national policies concerning the tobacco industry during the runtime of The College News (1914-1968).
  To take the next step with my data, I imported my csv file containing the results of the keyword search to [Pandas](https://pandas.pydata.org/), a python library for data analysis, as a DataFrame, and calculated the relative frequency of smoking and cigarette by dividing their yearly counts by the total wordcount of all College News issues published that year.
  Finally, I graphed my data using [Altair](https://altair-viz.github.io/), a python library for interactive data visualization, to make the bar graph above (to be elaborated, and if i manage to have D3 load my data I'll do a screenshot of my graph and put it here as well).



  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega@5"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-lite@4.8.1"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-embed@6"></script>
  <script>
  
    (function(vegaEmbed) {
      var spec = {
  "config": {
    "view": {"continuousWidth": 400, "continuousHeight": 300, "strokeWidth": 0},
    "axis": {"grid": false}
  },
  "data": {"name": "data-0b5625db42c83f249625f7c34b292cc9"},
  "mark": {"type": "bar", "color": "#2F04AC", "size": 15},
  "encoding": {
    "tooltip": [
      {"type": "quantitative", "field": "year"},
      {"type": "quantitative", "field": "relative_frequency"}
    ],
    "x": {"type": "quantitative", "axis": {"title": "Year"}, "field": "year"},
    "y": {
      "type": "quantitative",
      "axis": {"format": "%", "title": "Relative Frequency"},
      "field": "relative_frequency"
    }
  },
  "width": 1000,
  "$schema": "https://vega.github.io/schema/vega-lite/v4.8.1.json",
  "datasets": {
    "data-0b5625db42c83f249625f7c34b292cc9": [
      {"year": 1914, "relative_frequency": 0},
      {"year": 1915, "relative_frequency": 0.00000901},
      {"year": 1916, "relative_frequency": 0.0000044},
      {"year": 1917, "relative_frequency": 0},
      {"year": 1918, "relative_frequency": 0.0000065},
      {"year": 1919, "relative_frequency": 0.0000106},
      {"year": 1920, "relative_frequency": 0.0000101},
      {"year": 1921, "relative_frequency": 0.0000158},
      {"year": 1922, "relative_frequency": 0.0000364},
      {"year": 1923, "relative_frequency": 0.0000135},
      {"year": 1924, "relative_frequency": 0.0000169},
      {"year": 1925, "relative_frequency": 0.000165091},
      {"year": 1926, "relative_frequency": 0.0000541},
      {"year": 1927, "relative_frequency": 0.0000774},
      {"year": 1928, "relative_frequency": 0.000117779},
      {"year": 1929, "relative_frequency": 0.000171969},
      {"year": 1930, "relative_frequency": 0.0001555},
      {"year": 1931, "relative_frequency": 0.00033212},
      {"year": 1932, "relative_frequency": 0.000165175},
      {"year": 1933, "relative_frequency": 0.000316664},
      {"year": 1934, "relative_frequency": 0.00025019},
      {"year": 1935, "relative_frequency": 0.000180602},
      {"year": 1936, "relative_frequency": 0.000264716},
      {"year": 1937, "relative_frequency": 0.000211012},
      {"year": 1938, "relative_frequency": 0.000342496},
      {"year": 1939, "relative_frequency": 0.000296537},
      {"year": 1940, "relative_frequency": 0.000449125},
      {"year": 1941, "relative_frequency": 0.000236879},
      {"year": 1942, "relative_frequency": 0.000232155},
      {"year": 1943, "relative_frequency": 0.000301837},
      {"year": 1944, "relative_frequency": 0.000243905},
      {"year": 1945, "relative_frequency": 0.000193573},
      {"year": 1946, "relative_frequency": 0.000131988},
      {"year": 1947, "relative_frequency": 0.000252575},
      {"year": 1948, "relative_frequency": 0.000276802},
      {"year": 1949, "relative_frequency": 0.000191101},
      {"year": 1950, "relative_frequency": 0.000330139},
      {"year": 1951, "relative_frequency": 0.000329123},
      {"year": 1952, "relative_frequency": 0.000239171},
      {"year": 1953, "relative_frequency": 0.000353147},
      {"year": 1954, "relative_frequency": 0.000420463},
      {"year": 1955, "relative_frequency": 0.000448495},
      {"year": 1956, "relative_frequency": 0.000346263},
      {"year": 1957, "relative_frequency": 0.000188776},
      {"year": 1958, "relative_frequency": 0.000190097},
      {"year": 1959, "relative_frequency": 0.0000912},
      {"year": 1960, "relative_frequency": 0.0000627},
      {"year": 1961, "relative_frequency": 0.000130471},
      {"year": 1962, "relative_frequency": 0.00011425},
      {"year": 1963, "relative_frequency": 0.000091},
      {"year": 1964, "relative_frequency": 0.0000148},
      {"year": 1965, "relative_frequency": 0.0000967},
      {"year": 1966, "relative_frequency": 0.0000426},
      {"year": 1967, "relative_frequency": 0.0000702},
      {"year": 1968, "relative_frequency": 0.0000216}
    ]
  }
};
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
