# 箱型图-极坐标


----


## code

```html
<div id="c1">
</div>
```

```js
import data from '../data/diamond.json';
var G2 = require('g2');
var Stat = G2.Stat;
var chart = new G2.Chart({
  id: 'c1',
  width: 1000,
  height: 500,
  plotCfg: {
    margin: [20, 90, 60, 80]
  }
});
chart.source(data);
chart.coord('polar');
chart.schema().position(Stat.bin.quantile.letter('cut*price')).color('cut').shape('box');
chart.render();
```
