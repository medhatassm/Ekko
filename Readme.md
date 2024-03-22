# Ekko Website Template

On this website, I am gonna share everything about my life. Books I am reading, Games I am Playing, Stories and Events, it is like a portfolio but it is something a little personal.

> [!tip]
> This a clone project to practice my skills in CSS & HTML.
> This project will be updated with js when I finish learning it.

**I will explain everything I coded to make this repository as a recourse guide to check it later.**

## Table of Content
- [Header](#Header)
- [Landing Section](#Landing-Section)

## Let's Start 💥

### Prepare the Started file for a project.

- Create My HTML file and type my head content that it has:

  1. [Normalize](https://necolas.github.io/normalize.css/) CSS File: to make all content get a default property value.
  2. Font Awesome CDN: to use the icon from [font-awesome](https://fontawesome.com/) website.
  3. [Google Font](https://fonts.google.com/): using Cairo font style for all element in website.
  4. Main CSS File: the main CSS style for the whole project.
     _(Whole work in this file)_

- in the Main CSS file I create some global rules to make everything ready for development:

  1. set the `box-sizing` property value to `border-box` and make the prefix code for it to all elements.

  2. using `scroll-behavior` to make the scroll in the website smooth and look good.

  3. reset the style of ul (because we will use it a lot).

  4. set `font-family` to (Cairo) for `body`.

  5. make a container class to make sure my element will be in grid design and have the same padding and margin in all screen sizes, and make sure that the element height will not be less than 100px.

```
    .container {
    padding-left: 15px;
    padding-right: 15px;
    margin-left: auto;
    margin-right: auto;
    min-height: 97px;
}

/* Small */
@media (min-width: 768px) {
    .container {
        width: 750px;
    }
}

/* Medium */
@media (min-width: 992px) {
    .container {
        width: 970px;
    }
}

/* Large */
@media (min-width: 1200px) {
    .container {
        width: 1170px;
    }
}

```

### Header

The header has the logo & navigation links to sections in the website.

1. first we make the header `position` relative to make it take all the width of the screen without interfering property of our container (padding, margin).

2. then I create a box-shadow to make the header look like a navigation bar (stander design).

3. after that I make the container flex to make elements inside it get next to each other and make it wrap for mobile screen (not in media query).

```
.header {
    box-shadow: 0 0 10px #ddd;
    position: relative;
}

.header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    position: relative;
}
```

- Logo:

  I made a logo because it is just text without any image on it, so we can edit that to make it look as we want, and clickable to go to the link (same home page).

1. using `text-decoration` to erase all anchor default designs.

```
.header .container .logo {
    text-decoration: none;
    ...
     }
```

2. make it flexible to set height and make the text center (vertical & horizontal), in a mobile screen this element will have 50px of `height` and 100% of `width`, to make the header vertical in a small screen (768px).

```
.header .container .logo {
   ...
    display: flex;
    justify-content: center;
    align-items: center;
}
```

- Links:

  These links will be the navigator tools to go to web sections with just one click.

1. I make `ul` flex to make links inside it line up horizontally, in the mobile screen I make this element have `margin` auto to make it center when it has full width.

2. the `a` inside item of `ul` has 72px of height to change the background color when the user hovers on it, and it flexes to center the text inside it like a logo, on a small screen I change the (`padding`, `font-size`, `height`) to make look better in the small screen using media query.

3. give these links a `transition` to make animation when the user hovers over it.

4. Use `::before` to make a line that has `width:0` and when the user hovers the link it will increase to `width:100%` in `0.3s`.

```
.header .container ul li a::before {
    content: '';
    background-color: var(--main-color);
    width: 0;
    height: 4px;
    position: absolute;
    top: 0;
    left: 0;
    transition: var(--transition-value);
}
```

5. using `:hover` to make all animation we prepare work.

```
.header .container ul li a:hover {
    background-color: #f9f9f9;
    color: var(--main-color);
}

.header .container ul li a:hover::before {
    width: 100%;
}

```

### Landing Section
