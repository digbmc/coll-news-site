---
title: Political Topics from the 50s and 60s
layout: project
subtitle: Lorem ipsum dolor sit amet consectetur.
author:
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
        "color": {"type": "nominal", "field": "topics"},
        "opacity": {"value": 0},
        "tooltip": [
          {"type": "nominal", "field": "topics"},
          {"type": "quantitative", "field": "year"},
          {"type": "quantitative", "field": "frequency"}
        ],
        "x": {
          "type": "quantitative",
          "axis": {"labels": true},
          "field": "year",
          "scale": {"domain": [1950, 1968]}
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
          "fields": ["topics"],
          "nearest": true
        }
      },
      "width": 600
    },
    {
      "mark": {"type": "line", "size": 80},
      "encoding": {
        "color": {"type": "nominal", "field": "topics"},
        "size": {
          "condition": {"value": 1, "selection": {"not": "selector001"}},
          "value": 3
        },
        "x": {
          "type": "quantitative",
          "axis": {"labels": true},
          "field": "year",
          "scale": {"domain": [1950, 1968]}
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
  "data": {"name": "data-f8992e10ceec51faf6149a6c3a6fad0c"},
  "$schema": "https://vega.github.io/schema/vega-lite/v4.8.1.json",
  "datasets": {
    "data-f8992e10ceec51faf6149a6c3a6fad0c": [
      {
        "year": 1950,
        "frequency": 0.08365528,
        "topics": "0 political policy president"
      },
      {
        "year": 1951,
        "frequency": 0.086651768,
        "topics": "0 political policy president"
      },
      {
        "year": 1952,
        "frequency": 0.10245801,
        "topics": "0 political policy president"
      },
      {
        "year": 1953,
        "frequency": 0.095670854,
        "topics": "0 political policy president"
      },
      {
        "year": 1954,
        "frequency": 0.091141254,
        "topics": "0 political policy president"
      },
      {
        "year": 1955,
        "frequency": 0.108422952,
        "topics": "0 political policy president"
      },
      {
        "year": 1956,
        "frequency": 0.133524831,
        "topics": "0 political policy president"
      },
      {
        "year": 1957,
        "frequency": 0.094296642,
        "topics": "0 political policy president"
      },
      {
        "year": 1958,
        "frequency": 0.092239324,
        "topics": "0 political policy president"
      },
      {
        "year": 1959,
        "frequency": 0.102711491,
        "topics": "0 political policy president"
      },
      {
        "year": 1960,
        "frequency": 0.117320309,
        "topics": "0 political policy president"
      },
      {
        "year": 1961,
        "frequency": 0.115216605,
        "topics": "0 political policy president"
      },
      {
        "year": 1962,
        "frequency": 0.134210709,
        "topics": "0 political policy president"
      },
      {
        "year": 1963,
        "frequency": 0.103588938,
        "topics": "0 political policy president"
      },
      {
        "year": 1964,
        "frequency": 0.12677287,
        "topics": "0 political policy president"
      },
      {
        "year": 1965,
        "frequency": 0.108846218,
        "topics": "0 political policy president"
      },
      {
        "year": 1966,
        "frequency": 0.098047314,
        "topics": "0 political policy president"
      },
      {
        "year": 1967,
        "frequency": 0.101747903,
        "topics": "0 political policy president"
      },
      {
        "year": 1968,
        "frequency": 0.116105099,
        "topics": "0 political policy president"
      },
      {
        "year": 1950,
        "frequency": 0.07359118,
        "topics": "1 american africa country"
      },
      {
        "year": 1951,
        "frequency": 0.063181311,
        "topics": "1 american africa country"
      },
      {
        "year": 1952,
        "frequency": 0.070181935,
        "topics": "1 american africa country"
      },
      {
        "year": 1953,
        "frequency": 0.082931046,
        "topics": "1 american africa country"
      },
      {
        "year": 1954,
        "frequency": 0.081918462,
        "topics": "1 american africa country"
      },
      {
        "year": 1955,
        "frequency": 0.075185207,
        "topics": "1 american africa country"
      },
      {
        "year": 1956,
        "frequency": 0.062703472,
        "topics": "1 american africa country"
      },
      {
        "year": 1957,
        "frequency": 0.075508239,
        "topics": "1 american africa country"
      },
      {
        "year": 1958,
        "frequency": 0.0788983,
        "topics": "1 american africa country"
      },
      {
        "year": 1959,
        "frequency": 0.084398451,
        "topics": "1 american africa country"
      },
      {
        "year": 1960,
        "frequency": 0.087377347,
        "topics": "1 american africa country"
      },
      {
        "year": 1961,
        "frequency": 0.079291544,
        "topics": "1 american africa country"
      },
      {
        "year": 1962,
        "frequency": 0.07053521,
        "topics": "1 american africa country"
      },
      {
        "year": 1963,
        "frequency": 0.083436823,
        "topics": "1 american africa country"
      },
      {
        "year": 1964,
        "frequency": 0.05878277,
        "topics": "1 american africa country"
      },
      {
        "year": 1965,
        "frequency": 0.059878124,
        "topics": "1 american africa country"
      },
      {
        "year": 1966,
        "frequency": 0.085051282,
        "topics": "1 american africa country"
      },
      {
        "year": 1967,
        "frequency": 0.065736734,
        "topics": "1 american africa country"
      },
      {
        "year": 1968,
        "frequency": 0.066359901,
        "topics": "1 american africa country"
      },
      {"year": 1950, "frequency": 0.173987847, "topics": "3 world mr war"},
      {"year": 1951, "frequency": 0.2088206, "topics": "3 world mr war"},
      {"year": 1952, "frequency": 0.181735997, "topics": "3 world mr war"},
      {"year": 1953, "frequency": 0.183377615, "topics": "3 world mr war"},
      {"year": 1954, "frequency": 0.175326017, "topics": "3 world mr war"},
      {"year": 1955, "frequency": 0.165509376, "topics": "3 world mr war"},
      {"year": 1956, "frequency": 0.183958095, "topics": "3 world mr war"},
      {"year": 1957, "frequency": 0.176985286, "topics": "3 world mr war"},
      {"year": 1958, "frequency": 0.167609681, "topics": "3 world mr war"},
      {"year": 1959, "frequency": 0.199395574, "topics": "3 world mr war"},
      {"year": 1960, "frequency": 0.199123296, "topics": "3 world mr war"},
      {"year": 1961, "frequency": 0.197880655, "topics": "3 world mr war"},
      {"year": 1962, "frequency": 0.190216437, "topics": "3 world mr war"},
      {"year": 1963, "frequency": 0.13885432, "topics": "3 world mr war"},
      {"year": 1964, "frequency": 0.11948527, "topics": "3 world mr war"},
      {"year": 1965, "frequency": 0.156991457, "topics": "3 world mr war"},
      {"year": 1966, "frequency": 0.151631655, "topics": "3 world mr war"},
      {"year": 1967, "frequency": 0.161773414, "topics": "3 world mr war"},
      {"year": 1968, "frequency": 0.158035185, "topics": "3 world mr war"},
      {
        "year": 1950,
        "frequency": 0.081879226,
        "topics": "6 civil state government"
      },
      {
        "year": 1951,
        "frequency": 0.09916593,
        "topics": "6 civil state government"
      },
      {
        "year": 1952,
        "frequency": 0.084749929,
        "topics": "6 civil state government"
      },
      {
        "year": 1953,
        "frequency": 0.085430004,
        "topics": "6 civil state government"
      },
      {
        "year": 1954,
        "frequency": 0.092161141,
        "topics": "6 civil state government"
      },
      {
        "year": 1955,
        "frequency": 0.080549893,
        "topics": "6 civil state government"
      },
      {
        "year": 1956,
        "frequency": 0.114679453,
        "topics": "6 civil state government"
      },
      {
        "year": 1957,
        "frequency": 0.083694652,
        "topics": "6 civil state government"
      },
      {
        "year": 1958,
        "frequency": 0.077636525,
        "topics": "6 civil state government"
      },
      {
        "year": 1959,
        "frequency": 0.089162468,
        "topics": "6 civil state government"
      },
      {
        "year": 1960,
        "frequency": 0.116001684,
        "topics": "6 civil state government"
      },
      {
        "year": 1961,
        "frequency": 0.09701756,
        "topics": "6 civil state government"
      },
      {
        "year": 1962,
        "frequency": 0.129575398,
        "topics": "6 civil state government"
      },
      {
        "year": 1963,
        "frequency": 0.116972183,
        "topics": "6 civil state government"
      },
      {
        "year": 1964,
        "frequency": 0.139502904,
        "topics": "6 civil state government"
      },
      {
        "year": 1965,
        "frequency": 0.11302331,
        "topics": "6 civil state government"
      },
      {
        "year": 1966,
        "frequency": 0.100065294,
        "topics": "6 civil state government"
      },
      {
        "year": 1967,
        "frequency": 0.139377943,
        "topics": "6 civil state government"
      },
      {
        "year": 1968,
        "frequency": 0.131244364,
        "topics": "6 civil state government"
      }
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
