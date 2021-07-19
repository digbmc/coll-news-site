---
title: Political Topics from the 50s and 60s
layout: project
subtitle: Lorem ipsum dolor sit amet consectetur.
image:
alt: 

caption:
  title: Political topics
  subtitle: Issues 1950-1968
  thumbnail: assets/img/portfolio/50s60s-viz-thumb.png
  alt: data visualization of 50s and 60s topics

---

 <div id="vis"></div>

Use this area to describe your project. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est blanditiis dolorem culpa incidunt minus dignissimos deserunt repellat aperiam quasi sunt officia expedita beatae cupiditate, maiores repudiandae, nostrum, reiciendis facere nemo!


<script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega@5"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-lite@4.8.1"></script>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/npm//vega-embed@6"></script>

  <script>
    (function(vegaEmbed) {
      var spec = {
  "config": {"view": {"continuousWidth": 400, "continuousHeight": 300}},
  "layer": [
    {
      "mark": {"type": "circle", "size": 100},
      "encoding": {
        "color": {"type": "nominal", "field": "topic"},
        "opacity": {"value": 0},
        "tooltip": [
          {"type": "nominal", "field": "topic"},
          {"type": "quantitative", "field": "year"},
          {"type": "quantitative", "field": "frequency"}
        ],
        "x": {
          "type": "quantitative",
          "axis": {"labels": true},
          "field": "year",
          "scale": {"domain": [1950, 1967]}
        },
        "y": {
          "type": "quantitative",
          "axis": {"format": "%"},
          "field": "frequency"
        }
      },
      "selection": {
        "selector001": {
          "type": "single",
          "on": "mouseover",
          "fields": ["topic"],
          "nearest": true
        }
      },
      "width": 600
    },
    {
      "mark": {"type": "line", "size": 80},
      "encoding": {
        "color": {"type": "nominal", "field": "topic"},
        "size": {
          "condition": {"value": 1, "selection": {"not": "selector001"}},
          "value": 3
        },
        "x": {
          "type": "quantitative",
          "axis": {"labels": true},
          "field": "year",
          "scale": {"domain": [1950, 1967]}
        },
        "y": {
          "type": "quantitative",
          "axis": {"format": "%"},
          "field": "frequency"
        }
      },
      "selection": {
        "selector002": {
          "type": "interval",
          "bind": "scales",
          "encodings": ["x", "y"]
        }
      }
    }
  ],
  "data": {"name": "data-9c9fbe98d6191896154534b6db0223ca"},
  "$schema": "https://vega.github.io/schema/vega-lite/v4.8.1.json",
  "datasets": {
    "data-9c9fbe98d6191896154534b6db0223ca": [
      {"year": 1950, "frequency": 0.081670558, "topic": "civil rights"},
      {"year": 1950, "frequency": 0.107010129, "topic": "cold war"},
      {"year": 1951, "frequency": 0.108527021, "topic": "civil rights"},
      {"year": 1951, "frequency": 0.145990649, "topic": "cold war"},
      {"year": 1952, "frequency": 0.102362836, "topic": "civil rights"},
      {"year": 1952, "frequency": 0.125769481, "topic": "cold war"},
      {"year": 1953, "frequency": 0.09639816, "topic": "civil rights"},
      {"year": 1953, "frequency": 0.140484645, "topic": "cold war"},
      {"year": 1954, "frequency": 0.104066288, "topic": "civil rights"},
      {"year": 1954, "frequency": 0.127393156, "topic": "cold war"},
      {"year": 1955, "frequency": 0.090885213, "topic": "civil rights"},
      {"year": 1955, "frequency": 0.105609867, "topic": "cold war"},
      {"year": 1956, "frequency": 0.113696996, "topic": "civil rights"},
      {"year": 1956, "frequency": 0.149233327, "topic": "cold war"},
      {"year": 1957, "frequency": 0.095119468, "topic": "civil rights"},
      {"year": 1957, "frequency": 0.099037657, "topic": "cold war"},
      {"year": 1958, "frequency": 0.087008945, "topic": "civil rights"},
      {"year": 1958, "frequency": 0.087883861, "topic": "cold war"},
      {"year": 1959, "frequency": 0.089814217, "topic": "civil rights"},
      {"year": 1959, "frequency": 0.098714898, "topic": "cold war"},
      {"year": 1960, "frequency": 0.115720594, "topic": "civil rights"},
      {"year": 1960, "frequency": 0.123636352, "topic": "cold war"},
      {"year": 1961, "frequency": 0.105210562, "topic": "civil rights"},
      {"year": 1961, "frequency": 0.114448763, "topic": "cold war"},
      {"year": 1962, "frequency": 0.121924084, "topic": "civil rights"},
      {"year": 1962, "frequency": 0.149247509, "topic": "cold war"},
      {"year": 1963, "frequency": 0.12211834, "topic": "civil rights"},
      {"year": 1963, "frequency": 0.094671755, "topic": "cold war"},
      {"year": 1964, "frequency": 0.150251707, "topic": "civil rights"},
      {"year": 1964, "frequency": 0.083180511, "topic": "cold war"},
      {"year": 1965, "frequency": 0.115189529, "topic": "civil rights"},
      {"year": 1965, "frequency": 0.083056449, "topic": "cold war"},
      {"year": 1966, "frequency": 0.098535838, "topic": "civil rights"},
      {"year": 1966, "frequency": 0.099369118, "topic": "cold war"},
      {"year": 1967, "frequency": 0.107509786, "topic": "civil rights"},
      {"year": 1967, "frequency": 0.088230678, "topic": "cold war"}
    ]
  }
};

  var embedOpt = {"renderer": "svg", "mode": "vega-lite"};
  
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
