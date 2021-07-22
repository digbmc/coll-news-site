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



### Topics:

0.	political policy president government conference alliance party gov mr foreign united news states discussion general affairs national issue state issues
1.	american africa country europe south world west east york travel french home days time city african france _ trip air
3.	world mr war people united states man peace great country con problem life time today nations ing china problems ed
4.	school scholarship york scholar high prepared mary pennsylvania ann elizabeth jane alumnae national regional college anne nancy rhoads barbara city
5.	students bryn mawr student college year campus work committee program haverford colleges group class service school faculty ing summer stu
6.	civil state government rights negro people ment law public social american south action labor tion white aid education support union
7.	play world good man show time ing life love story audience don men played cigarette part stage great back young
8.	mr university american dr professor history science miss department art english work political research study philosophy de college mrs mawr
    The abundance of stop words and OCR noise in The College News predicates that the topic modeling tool, when analyzing our corpus, won’t always produce meaningful results. Therefore, we have chosen to only visualize topics containing meaningful content. There are two topics excluded from the line chart due to their lack of specific information: “2. college mawr bryn news ee pa ardmore 5 ave editor ae page 3 year 2 1 company lancaster wednesday weeks” and “9. page 30 8 1 continued 4 2 room 5 col 3 00 7 music april march 15 6 common friday”.


### x-axis: timeline and its context

  Our timeline starts from years 1950 and ends in year 1968, when the Bryn Mawr College News merged with Haverford’s student newspaper. We have chosen this time period for our political topics visualization because we are aware of the history backdrop of the Cold War, Vietnam war, and civil rights movement, and therefore interested in investigating the political awareness and engagement in the Bryn Mawr community during this period of political and social change.
    
    
### y-axis: relative frequency

   The relative frequency of a topic in a chunk of text refers to the number of words dedicated to this topic divided by the total wordcount in a given chunk. The topic modeling tool computes the relative frequency of topics per chunk as a part of its output. We then calculated the relative frequency of topics each year by finding the mean of relative frequency in chunks published in that year.
    
    
### Topic Modeling

   Topic Modeling allows us to analyze our large corpus through extracting topics. A "topic" consists of a cluster of words that frequently occur together. This form of computational text analysis relies on an algorithm called “Latent Dirichlet Allocation” and contains an aleatory aspect. Therefore, despite using the same corpus as the input, the output of topic modeling will be slightly different every time.
    
    
### Our Approach

   We uploaded our entire corpus into the topic modeling tool and adjusted the setting to divide the text into chunks of 500 characters. In doing so, we allowed the topic modeling tool to identify words appearing in each other’s vicinity instead of simply coexistent words in the entire College News issue. The topic modeling tool generated 10 topics for the whole corpus. We identified one of these topics to be political and used its cluster of words to run keyword search through all text chunks. All chunks containing one or more of these keywords were sorted into a separate directory. This directory is used as the new input of the topic modeling tool in order to obtain more politics-focused results. The final output contains three political topics out of ten in total.
    
    
### Visualization:
   We graphed the data using Altair, a python library for data visualization based on Vega and Vega-lite. We chose a line chart because we would like to investigate whether a pattern or trend exists in a given topic.




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
          {"type": "quantitative", "field": "relative frequency"}
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
          "field": "relative frequency"
        }
      },
      "selection": {
        "selector005": {
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
          "condition": {"value": 1, "selection": {"not": "selector005"}},
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
          "field": "relative frequency"
        }
      },
      "selection": {
        "selector006": {
          "type": "interval",
          "bind": "scales",
          "encodings": ["x", "y"]
        }
      }
    }
  ],
  "data": {"name": "data-d86eab4150a1c52123f96c7fcf7bde51"},
  "$schema": "https://vega.github.io/schema/vega-lite/v4.8.1.json",
  "datasets": {
    "data-d86eab4150a1c52123f96c7fcf7bde51": [
      {
        "year": 1950,
        "relative frequency": 0.08365528,
        "topics": "0 political policy president"
      },
      {
        "year": 1951,
        "relative frequency": 0.086651768,
        "topics": "0 political policy president"
      },
      {
        "year": 1952,
        "relative frequency": 0.10245801,
        "topics": "0 political policy president"
      },
      {
        "year": 1953,
        "relative frequency": 0.095670854,
        "topics": "0 political policy president"
      },
      {
        "year": 1954,
        "relative frequency": 0.091141254,
        "topics": "0 political policy president"
      },
      {
        "year": 1955,
        "relative frequency": 0.108422952,
        "topics": "0 political policy president"
      },
      {
        "year": 1956,
        "relative frequency": 0.133524831,
        "topics": "0 political policy president"
      },
      {
        "year": 1957,
        "relative frequency": 0.094296642,
        "topics": "0 political policy president"
      },
      {
        "year": 1958,
        "relative frequency": 0.092239324,
        "topics": "0 political policy president"
      },
      {
        "year": 1959,
        "relative frequency": 0.102711491,
        "topics": "0 political policy president"
      },
      {
        "year": 1960,
        "relative frequency": 0.117320309,
        "topics": "0 political policy president"
      },
      {
        "year": 1961,
        "relative frequency": 0.115216605,
        "topics": "0 political policy president"
      },
      {
        "year": 1962,
        "relative frequency": 0.134210709,
        "topics": "0 political policy president"
      },
      {
        "year": 1963,
        "relative frequency": 0.103588938,
        "topics": "0 political policy president"
      },
      {
        "year": 1964,
        "relative frequency": 0.12677287,
        "topics": "0 political policy president"
      },
      {
        "year": 1965,
        "relative frequency": 0.108846218,
        "topics": "0 political policy president"
      },
      {
        "year": 1966,
        "relative frequency": 0.098047314,
        "topics": "0 political policy president"
      },
      {
        "year": 1967,
        "relative frequency": 0.101747903,
        "topics": "0 political policy president"
      },
      {
        "year": 1968,
        "relative frequency": 0.116105099,
        "topics": "0 political policy president"
      },
      {
        "year": 1950,
        "relative frequency": 0.07359118,
        "topics": "1 american africa country"
      },
      {
        "year": 1951,
        "relative frequency": 0.063181311,
        "topics": "1 american africa country"
      },
      {
        "year": 1952,
        "relative frequency": 0.070181935,
        "topics": "1 american africa country"
      },
      {
        "year": 1953,
        "relative frequency": 0.082931046,
        "topics": "1 american africa country"
      },
      {
        "year": 1954,
        "relative frequency": 0.081918462,
        "topics": "1 american africa country"
      },
      {
        "year": 1955,
        "relative frequency": 0.075185207,
        "topics": "1 american africa country"
      },
      {
        "year": 1956,
        "relative frequency": 0.062703472,
        "topics": "1 american africa country"
      },
      {
        "year": 1957,
        "relative frequency": 0.075508239,
        "topics": "1 american africa country"
      },
      {
        "year": 1958,
        "relative frequency": 0.0788983,
        "topics": "1 american africa country"
      },
      {
        "year": 1959,
        "relative frequency": 0.084398451,
        "topics": "1 american africa country"
      },
      {
        "year": 1960,
        "relative frequency": 0.087377347,
        "topics": "1 american africa country"
      },
      {
        "year": 1961,
        "relative frequency": 0.079291544,
        "topics": "1 american africa country"
      },
      {
        "year": 1962,
        "relative frequency": 0.07053521,
        "topics": "1 american africa country"
      },
      {
        "year": 1963,
        "relative frequency": 0.083436823,
        "topics": "1 american africa country"
      },
      {
        "year": 1964,
        "relative frequency": 0.05878277,
        "topics": "1 american africa country"
      },
      {
        "year": 1965,
        "relative frequency": 0.059878124,
        "topics": "1 american africa country"
      },
      {
        "year": 1966,
        "relative frequency": 0.085051282,
        "topics": "1 american africa country"
      },
      {
        "year": 1967,
        "relative frequency": 0.065736734,
        "topics": "1 american africa country"
      },
      {
        "year": 1968,
        "relative frequency": 0.066359901,
        "topics": "1 american africa country"
      },
      {
        "year": 1950,
        "relative frequency": 0.173987847,
        "topics": "3 world mr war"
      },
      {
        "year": 1951,
        "relative frequency": 0.2088206,
        "topics": "3 world mr war"
      },
      {
        "year": 1952,
        "relative frequency": 0.181735997,
        "topics": "3 world mr war"
      },
      {
        "year": 1953,
        "relative frequency": 0.183377615,
        "topics": "3 world mr war"
      },
      {
        "year": 1954,
        "relative frequency": 0.175326017,
        "topics": "3 world mr war"
      },
      {
        "year": 1955,
        "relative frequency": 0.165509376,
        "topics": "3 world mr war"
      },
      {
        "year": 1956,
        "relative frequency": 0.183958095,
        "topics": "3 world mr war"
      },
      {
        "year": 1957,
        "relative frequency": 0.176985286,
        "topics": "3 world mr war"
      },
      {
        "year": 1958,
        "relative frequency": 0.167609681,
        "topics": "3 world mr war"
      },
      {
        "year": 1959,
        "relative frequency": 0.199395574,
        "topics": "3 world mr war"
      },
      {
        "year": 1960,
        "relative frequency": 0.199123296,
        "topics": "3 world mr war"
      },
      {
        "year": 1961,
        "relative frequency": 0.197880655,
        "topics": "3 world mr war"
      },
      {
        "year": 1962,
        "relative frequency": 0.190216437,
        "topics": "3 world mr war"
      },
      {
        "year": 1963,
        "relative frequency": 0.13885432,
        "topics": "3 world mr war"
      },
      {
        "year": 1964,
        "relative frequency": 0.11948527,
        "topics": "3 world mr war"
      },
      {
        "year": 1965,
        "relative frequency": 0.156991457,
        "topics": "3 world mr war"
      },
      {
        "year": 1966,
        "relative frequency": 0.151631655,
        "topics": "3 world mr war"
      },
      {
        "year": 1967,
        "relative frequency": 0.161773414,
        "topics": "3 world mr war"
      },
      {
        "year": 1968,
        "relative frequency": 0.158035185,
        "topics": "3 world mr war"
      },
      {
        "year": 1950,
        "relative frequency": 0.054013408,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1951,
        "relative frequency": 0.054200035,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1952,
        "relative frequency": 0.050758324,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1953,
        "relative frequency": 0.049530987,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1954,
        "relative frequency": 0.058484904,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1955,
        "relative frequency": 0.056853691,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1956,
        "relative frequency": 0.042155025,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1957,
        "relative frequency": 0.049391381,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1958,
        "relative frequency": 0.057471941,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1959,
        "relative frequency": 0.04334427,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1960,
        "relative frequency": 0.052008227,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1961,
        "relative frequency": 0.045550592,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1962,
        "relative frequency": 0.030786545,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1963,
        "relative frequency": 0.035147406,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1964,
        "relative frequency": 0.039129844,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1965,
        "relative frequency": 0.041302412,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1966,
        "relative frequency": 0.034865645,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1967,
        "relative frequency": 0.028069225,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1968,
        "relative frequency": 0.038180821,
        "topics": "4 school scholarship york"
      },
      {
        "year": 1950,
        "relative frequency": 0.134212763,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1951,
        "relative frequency": 0.149932726,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1952,
        "relative frequency": 0.160560159,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1953,
        "relative frequency": 0.15222474,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1954,
        "relative frequency": 0.150886935,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1955,
        "relative frequency": 0.163840444,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1956,
        "relative frequency": 0.155177298,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1957,
        "relative frequency": 0.174368194,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1958,
        "relative frequency": 0.157345714,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1959,
        "relative frequency": 0.141813125,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1960,
        "relative frequency": 0.137382268,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1961,
        "relative frequency": 0.165499777,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1962,
        "relative frequency": 0.140437931,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1963,
        "relative frequency": 0.172116651,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1964,
        "relative frequency": 0.199879474,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1965,
        "relative frequency": 0.198776166,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1966,
        "relative frequency": 0.209394088,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1967,
        "relative frequency": 0.203103261,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1968,
        "relative frequency": 0.216403444,
        "topics": "5 students bryn mawr"
      },
      {
        "year": 1950,
        "relative frequency": 0.081879226,
        "topics": "6 civil state government"
      },
      {
        "year": 1951,
        "relative frequency": 0.09916593,
        "topics": "6 civil state government"
      },
      {
        "year": 1952,
        "relative frequency": 0.084749929,
        "topics": "6 civil state government"
      },
      {
        "year": 1953,
        "relative frequency": 0.085430004,
        "topics": "6 civil state government"
      },
      {
        "year": 1954,
        "relative frequency": 0.092161141,
        "topics": "6 civil state government"
      },
      {
        "year": 1955,
        "relative frequency": 0.080549893,
        "topics": "6 civil state government"
      },
      {
        "year": 1956,
        "relative frequency": 0.114679453,
        "topics": "6 civil state government"
      },
      {
        "year": 1957,
        "relative frequency": 0.083694652,
        "topics": "6 civil state government"
      },
      {
        "year": 1958,
        "relative frequency": 0.077636525,
        "topics": "6 civil state government"
      },
      {
        "year": 1959,
        "relative frequency": 0.089162468,
        "topics": "6 civil state government"
      },
      {
        "year": 1960,
        "relative frequency": 0.116001684,
        "topics": "6 civil state government"
      },
      {
        "year": 1961,
        "relative frequency": 0.09701756,
        "topics": "6 civil state government"
      },
      {
        "year": 1962,
        "relative frequency": 0.129575398,
        "topics": "6 civil state government"
      },
      {
        "year": 1963,
        "relative frequency": 0.116972183,
        "topics": "6 civil state government"
      },
      {
        "year": 1964,
        "relative frequency": 0.139502904,
        "topics": "6 civil state government"
      },
      {
        "year": 1965,
        "relative frequency": 0.11302331,
        "topics": "6 civil state government"
      },
      {
        "year": 1966,
        "relative frequency": 0.100065294,
        "topics": "6 civil state government"
      },
      {
        "year": 1967,
        "relative frequency": 0.139377943,
        "topics": "6 civil state government"
      },
      {
        "year": 1968,
        "relative frequency": 0.131244364,
        "topics": "6 civil state government"
      },
      {
        "year": 1950,
        "relative frequency": 0.146213785,
        "topics": "7 play world good"
      },
      {
        "year": 1951,
        "relative frequency": 0.108679548,
        "topics": "7 play world good"
      },
      {
        "year": 1952,
        "relative frequency": 0.117753744,
        "topics": "7 play world good"
      },
      {
        "year": 1953,
        "relative frequency": 0.107658936,
        "topics": "7 play world good"
      },
      {
        "year": 1954,
        "relative frequency": 0.104849347,
        "topics": "7 play world good"
      },
      {
        "year": 1955,
        "relative frequency": 0.104721779,
        "topics": "7 play world good"
      },
      {
        "year": 1956,
        "relative frequency": 0.09410365,
        "topics": "7 play world good"
      },
      {
        "year": 1957,
        "relative frequency": 0.110433939,
        "topics": "7 play world good"
      },
      {
        "year": 1958,
        "relative frequency": 0.114245013,
        "topics": "7 play world good"
      },
      {
        "year": 1959,
        "relative frequency": 0.120606773,
        "topics": "7 play world good"
      },
      {
        "year": 1960,
        "relative frequency": 0.096470997,
        "topics": "7 play world good"
      },
      {
        "year": 1961,
        "relative frequency": 0.091738374,
        "topics": "7 play world good"
      },
      {
        "year": 1962,
        "relative frequency": 0.08418157,
        "topics": "7 play world good"
      },
      {
        "year": 1963,
        "relative frequency": 0.10048931,
        "topics": "7 play world good"
      },
      {
        "year": 1964,
        "relative frequency": 0.095194117,
        "topics": "7 play world good"
      },
      {
        "year": 1965,
        "relative frequency": 0.099717008,
        "topics": "7 play world good"
      },
      {
        "year": 1966,
        "relative frequency": 0.090404743,
        "topics": "7 play world good"
      },
      {
        "year": 1967,
        "relative frequency": 0.090122053,
        "topics": "7 play world good"
      },
      {
        "year": 1968,
        "relative frequency": 0.079314559,
        "topics": "7 play world good"
      },
      {
        "year": 1950,
        "relative frequency": 0.102530396,
        "topics": "8 mr university american"
      },
      {
        "year": 1951,
        "relative frequency": 0.093085643,
        "topics": "8 mr university american"
      },
      {
        "year": 1952,
        "relative frequency": 0.08336631,
        "topics": "8 mr university american"
      },
      {
        "year": 1953,
        "relative frequency": 0.106708315,
        "topics": "8 mr university american"
      },
      {
        "year": 1954,
        "relative frequency": 0.092994027,
        "topics": "8 mr university american"
      },
      {
        "year": 1955,
        "relative frequency": 0.092580493,
        "topics": "8 mr university american"
      },
      {
        "year": 1956,
        "relative frequency": 0.073943734,
        "topics": "8 mr university american"
      },
      {
        "year": 1957,
        "relative frequency": 0.089967861,
        "topics": "8 mr university american"
      },
      {
        "year": 1958,
        "relative frequency": 0.104503668,
        "topics": "8 mr university american"
      },
      {
        "year": 1959,
        "relative frequency": 0.099291852,
        "topics": "8 mr university american"
      },
      {
        "year": 1960,
        "relative frequency": 0.08314103,
        "topics": "8 mr university american"
      },
      {
        "year": 1961,
        "relative frequency": 0.082040823,
        "topics": "8 mr university american"
      },
      {
        "year": 1962,
        "relative frequency": 0.088696409,
        "topics": "8 mr university american"
      },
      {
        "year": 1963,
        "relative frequency": 0.083743045,
        "topics": "8 mr university american"
      },
      {
        "year": 1964,
        "relative frequency": 0.079211114,
        "topics": "8 mr university american"
      },
      {
        "year": 1965,
        "relative frequency": 0.081310664,
        "topics": "8 mr university american"
      },
      {
        "year": 1966,
        "relative frequency": 0.088538357,
        "topics": "8 mr university american"
      },
      {
        "year": 1967,
        "relative frequency": 0.067925735,
        "topics": "8 mr university american"
      },
      {
        "year": 1968,
        "relative frequency": 0.081083167,
        "topics": "8 mr university american"
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
