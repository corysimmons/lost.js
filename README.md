<p align="center">
  <img src="http://corysimmons.github.io/lost-grid.js/lost-grid.js.svg">
</p>

lost-grid.js is a revolutionary grid system where you can **create your grid directly in your markup**. It's based off it's incredibly powerful CSS preprocessor sister, [Lost Grid](https://github.com/corysimmons/lost).

It uses similar markup to Bootstrap's grid (`container > row > columns`) so it's very easy to pick up. What sets it apart from Bootstrap's grid is it's ability to use fractions to create grids on-the-fly. Did we mention you can do all this directly in your markup?


### Installation
- Include jQuery
- Include [lost-grid.js](lost-grid.js)
- Include a stylesheet in your HTML file somewhere


### Getting Started
Let's start by creating 2 elements that are half of their container. Any fraction will work. Any amount of items will work.

```html
<section l-center>
  <div l-row>

    <figure l-column="1/2">...</figure>
    <figure l-column="1/2">...</figure>

  </div>
</section>
```

Let's offset an element. Pass a postive fraction to create a `margin-left` offset. Pass a negative one for `margin-right`.

```html
<figure l-column="1/3" l-offset="1/3">...</figure>
<figure l-column="1/3">...</figure>
```

We can source order with the `l-move` attribute.

```html
<figure l-column="1/2" l-move="1/2">1</figure>
<figure l-column="1/2" l-move="-1/2">2</figure>
```

lost-grid.js supports [Isotope](http://isotope.metafizzy.co/) for columns of unequal height, but in lieu of that, you can clear columns at a certain interval with the `l-cycle` attribute applied to a row.

```html
<section l-center>
  <div l-row l-cycle="3">

    <figure l-column="1/3">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est, facilis.
    </figure>
    <figure l-column="1/3">
      Lorem ipsum dolor.
    </figure>
    <figure l-column="1/3">
      Lorem ipsum dolor sit amet, consectetur adipisicing.
    </figure>

    <figure l-column="1/3">
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Est, facilis.
    </figure>

  </div>
</section>
```


### Settings
```javascript
var lost = {
  gutter: 0,
  breakpoint: 1000,
  rtl: false
};
```


### Browser Support
- IE9+
- Poor support in older Android browsers


### Caveats
- Although the grid you create is responsive, there is currently no support for breakpoints. We're currently working on an elegant solution to this problem.
