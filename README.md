# simple-js-lightbox

> A very simple lightbox for use with image galleries. 

Demo: [fredrikburmester.com](https://fredrikburmester.com)

## Info

This is a simple lightbox with support for lazy loading when scrolling through images, arrow keys and swiping on both mobile and desktop using the [Swipe](https://swipe.js.org/) library, [GitHub](https://github.com/lyfeyaj/swipe). 

Since this lightbox was made to work with lazy loading, the image links can not be taken directly from the gallery-image `src` tag, that means that we need to have a pre-defined list of all links to our images.

## How-to

1. To use this lightbox you need to have an array of the image-files with this structure:

```
var obj = [
    {
        'src': './img/1.jpg'
    },
    {
        'src': './img/2.jpg'
    }
]
```

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

4. Include `data-src` and `onclick()` attribute to gallery images: 
```
<img onclick="openLightbox("<image-number>")" data-src="./image-thumb.jpg" />
```

I don't have any `src` attribute in the `img` tag above since I want to dynamically add that, i.e. lazy-loading. But if you do not use lazy-loading in your gallery you can add the `src` attribute. The `data-src` tag still needs to be there though. 

## Release History

* 0.0.2
    * Removed a bug on mobile

* 0.0.1
    * Work in progress
    
## Bugs

[Fixed] There is a bug on mobile right now where touch is disabled after opening and closing the lightbox. Fixed by adding `display:none;` on the lightbox div. 

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request
