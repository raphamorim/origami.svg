# origami.svg

> Origamijs plugin to render canvas to SVG

Working only for [Origami.js](https://github.com/raphamorim/origami.js) >= 0.5.0

Originally a fork of [canvas2svg](https://github.com/gliffy/canvas2svg).

## Getting

First of all, get Origami.js using [Download Option](https://github.com/raphamorim/origami.js/archive/master.zip) or using NPM.

Get using NPM just run this command

```sh
npm install origamijs.svg
```

Add the source after origamijs script end:

```html
<script src="origami.js"></script>
<script src="origami.svg.js"></script>
</body>
```

## Using

After load, just use `svg` as argument in draw method:

```javascript

origami('#canvas-id')
  .border({
    border: '4px dotted #654'
  })
  .image('test/resources/image-1.jpg', '5%', '5%', 200, 200)
  .arc(100, 75, 50, {
    background: '#2A80B9',
    borderSize: '4px',
    borderColor: 'gold',
    borderStyle: 'dotted'
  })
  .rect(10, 10, 50, 100, {
    background: 'lightblue',
    border: '4px solid #999'
  })
  .rect(50, 10, 40, {
    background: 'lightgreen',
    border: '10px solid green'
  })
  .load(function(octx) {
    octx.draw('svg');
  });

```

##### Result:

![Result](https://raw.githubusercontent.com/origamijs/origami.svg/master/examples/result.jpg)
