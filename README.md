# Mixins

## +html
```jade
+html
```

```html
<!DOCTYPE html>
<html lang="en-us">

</html>
```

## +head
```jade
+head({ color: '#000', title: 'A title or something.', description: 'A description or something.' })
```

```html
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width" initial-scale="1">
  <meta name="theme-color" content="#000">
  <meta name="description" content="A description or something.">
  <title>A title or something.</title>
</head>
```

## +script

```jade
+script('path/to/script.js')
```

```html
<script src="path/to/script.js"></script>
```

## +style

```jade
+style('path/to/styles.css')
```

```html
<link href="path/to/styles.css" rel="stylesheet" type="text/css">
```

## +image

```jade
+image('path/to/image.png')
```

```html
<img src="path/to/image.png">
```

## +input

```jade
+input(type='text')
```

```html
<input size='1' type='text'>
```

## +video

```jade
+video
  source(src='path/to/video.mp4' type='video/mp4')
```

```html
<video width='auto' height='auto'>
  <source src='path/to/video.mp4' type='video/mp4'>
</video>
```

# SVG

## +svg

```jade
+svg.
  <symbol id='close' viewBox='0 0 16 16'>
    <path stroke='#f00' stroke-width='2' d='M4 4l8 8m0-8l-8 8' stroke-linecap='round'/>
  </symbol>
```

```html
<svg xmlns="http://www.w3.org/2000/svg" style="display: none">
  <symbol id='close' viewBox='0 0 16 16'>
    <path stroke='#f00' stroke-width='2' d='M4 4l8 8m0-8l-8 8' stroke-linecap='round'/>
  </symbol>
</svg>
```

## +use

```jade
+use('symbol-id')
```

```html
<svg>
  <use xlink:href='symbol-id'/>
</svg>
```

# Vue.js

## +vue

```jade
+vue({ id: 'app', script: 'main.js' })
  .foobar
```

```html
<body>
  <div id='root'>
    <div class='foobar'></div>
  </div>
  <script src='dist/build.js'></script>
</body>
```

## +template

```jade
+template('template-id')
  div This is a template!
```

```html
<script id='template-id' type='x/template'>
  <div>This is a template!</div>
</script>
```
