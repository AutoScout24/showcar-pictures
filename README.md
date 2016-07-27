# showcar-pictures

This module provides a easy to use vanilla js gallery library with previews and full screen view.
Actually it is just a wrapper that handles the communication between two [showcar-carousel](https://github.com/AutoScout24/showcar-carousel) components. 

***

## Usage

#####Live example:
Visit the [example](https://autoscout24.github.io/showcar-pictures/) on github pages.


#####Local example:
Just run the following command in the root of the carousel library.

```
$> npm start
```
This will open a small express server on your local machine where you can see the running example.

Visit: [http://localhost:8080](http://localhost:8080)

#### HTML Code

See the following example below:

```html

<as24-pictures class="as24-pictures">
  <div class="as24-pictures__header fullScreen-show">
    <div class="as24-pictures__header-line">
      <h2 class="as24-pictures__picture-title"><!-- Big title of the picture --></h2>
      <i class="as24-pictures__fullscreen-close"><!-- Close button text --></i>
    </div>
    <div class="as24-pictures__header-line">
      <h5 class="as24-pictures__picture-subtitle"><!-- Subtitle text --></h5>
    </div>
  </div>
  <div class="as24-pictures__content">
    <div class="as24-pictures__slider-container">
      <as24-carousel class="as24-pictures__slider" mode="slider" gap="0" preview="true" indicator="true">
        <div class="as24-carousel-item">
            <img class="as24-pictures__image"
                 <!-- The URL of a pic in preview mode -->
                 data-src="http://..."
                 <!-- The URL of a pic in fullscreen mode -->
                 data-fullscreen-src="http://..."
                 src=""
                 alt="">
        </div>
        <!-- more pics here -->
      </as24-carousel>
      <as24-carousel class="as24-pictures__thumbnails" gap="4">
        <div class="as24-carousel-item">
          <div class="as24-carousel-image-container">
            <img data-src="http://placehold.it/100x75/d91a2a/ffffff?text=1" src="" alt="">
          </div>
        </div>
        <!-- more thumbs here -->
      </as24-carousel>
    </div>
    <aside class="as24-pictures__info">
      <div class="car-info"><!-- space for car info --></div>
      <div class="ads"><!-- space for ads --></div>
    </aside>
  </div>
</as24-pictures>
```
*Note: The number of the thumbnails and the number of slides MUST be the same!*

#### CSS Styling 

As to styles, you only have to specify these:

```css
#my-pics .as24-pictures__slider .as24-carousel-container {
  height: 480px;
}
```

This one to know what is the height of the slider (and images as a result). As it might depend on a particular situation, we cannot fix it.

```css
#my-pics .as24-pictures__slider .as24-carousel-item {
  max-width: 640px;
}
```

As we also need to know the maximal width of the an image in the slider.

For more information on styling have a look at the [showcar-carousel](https://github.com/AutoScout24/showcar-carousel) documentation.

## Installation

#### How to install:

To install showcar-pictures within your project use npm.

```
$> npm install showcar-pictures --save
```

Afterwards you need to add some css and js to your page.

```html
<link rel="stylesheet" href="../dist/showcar-pictures.css">
<link rel="stylesheet" href="../dist/showcar-carousel.css">
```

```html
<script src="../dist/showcar-carousel.js"></script>
<script src="../dist/showcar-pictures.js"></script>
```

*Note: The showcar-pictures depends on the [showcar-carousel](https://github.com/AutoScout24/showcar-carousel) component.*

***

## Contributing

#### How to contribute:

* Fork this repository.      
* Then install the required dependencies.
    ```
    $> npm install 
    ```  
* Start the dev server.
    ```
    $> npm run dev
    ```
* Visit [http://localhost:8080](http://localhost:8080)

*Note: changes will automatically build and refresh the browser.*

##### Contribute

Save your changes and run `$> npm prod`.

Commit your code _and_ the compiled libraries in _./dist_. Then create a pull-request.

## License

MIT License
