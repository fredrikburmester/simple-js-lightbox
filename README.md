# simple-js-lightbox

> A very simple lightbox for use with image galleries. 

[fredrikburmester.com](https://fredrikburmester.com)

## Info

This is a super simple lightbox with support for arrow keys and swiping on both mobile and desktop using the [Swipe](https://swipe.js.org/) library, [GitHub](https://github.com/lyfeyaj/swipe). 

## How-to

1. To use this lightbox you need to have an array of the imagefiles with this structure:

`array['link'] = <link-to-the-image>`

2. You need to include the CSS and JS file in your base html file. 

```
<head>
  ...
  <link rel="stylesheet" href="./lightbox.css">
</head>
<body>
  ...
  <script src="./lightbox.js"></script>
</body>
```

3. Include a lightbox div in your body.


```
<body>
  <div id="lightbox" class="lightbox">
  <script src="./lightbox.js"></script>
</body>
```

And everything will just work!

## Release History

* 0.0.1
    * Work in progress
    
## Bugs

There is a bug on mobile right now where touch is disabled after opening and closing the lightbox.

## Contributing

1. Fork it (<https://github.com/fredrikburmester/fredrikburmester-django/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request
