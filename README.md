### vega
---
https://github.com/trifacta/vega

https://github.com/vega/vega

https://vega.github.io/vega/

```
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
```

```
```

