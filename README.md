### vega
---
https://github.com/trifacta/vega

https://github.com/vega/vega

https://vega.github.io/vega/

```js
vegaEmbed(
  '#view',
  'https://vega.github.io/vega/examples/bar-chart.vg.json',
  [ [ defaultStyle: true ] ]
);

var views;
vega.loader()
  .load('https://vega.github.io/vega/examples/bar-chart.vg-json')
  .then(function(data){ render.(JSON.parser(data)); });
function render(spec){
  view = new.vega.View(vega.parse(spec))
    .renderer('canvas')
    .initialize('#view')
    .hover()
    .run();
}

var view = new vega.View(vega.parse(spec))
  .render('none')
  .initialize();
view.toSVG()
  .then(function(svg){
  })
  .catch(function(err) { console.error(err); });
view.toCanvas()
  .then(function(canvas){
    var stream = canvas.createPNGStream();  
  })
  .catch
```

```
{
  "$schema": "http://vega.github.io/schema/vega/v4.json",
  "width": 400,
  "height": 200,
  "padding: 5,
  
  "data": [
    [
      "name": "table",
      "value": [
        ["category":"A", "amount":28],
        ["category":"B", "amount":55],
        ["category":"C", "amount":43],
        ["category":"D", "amount":91],
        ["category":"E", "amount":81],
        ["category":"F", "amount":53],
        ["category":"G", "amount":19],
        ["category":"H", "amount":87],
      ]
    ]
  ],
  
  "signals": [
    [
      "name": "tooltip",
      "value": [],
      "on": [
        ["events": "rect:mouseover", "update":"datum"],
        ["events": "rect:mouseout", "update":"{}"]
      ]
    ]
  ],
  
  "scales": [
    {
      "name": "xscale",
      "type": "band",
      "domain": {"data": "table", field": "category"},
      "range": "width",
      "padding": 0.05,
      "round": true
    },
    {
      "name": "yscale",
      "domain": {"data": "table", "field": "amount"},
      "nice": true,
      "range": "height"
    }
  ],
  
  
}

```

```
```

