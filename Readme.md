# Ekko Website Template

In this website I am gonna share everything about my life. Books Iam reading, Games Iam Playing, Stories and Events, it is like a portfolio but it something little personal.

> [!tip]
> This a clone project to practice my skill in CSS & HTML.
> This project will be updated with js when i finish learn it.

**I will emplane everything i code it to make this repository as recourse guide to check it later.**

## Table of Content

[Header](#Header)
[[#Landing Section]]

## Let's Start 💥

### Prepare Started file for project.

- Create My HTML file and type my head content that it have:

  1. [Normalize](https://necolas.github.io/normalize.css/) CSS File: to make all content get default property value.
  2. Font Awesome CDN: to use icon from [font-awesome](https://fontawesome.com/) website.
  3. [Google Font](https://fonts.google.com/): using Cairo font style for all element in website.
  4. Main CSS File: the main css style fo whole project.
     _(Whole work in this file)_

- in Main CSS file i create some global rules to make every thing ready for development:

  1. set `box-sizing` property value to `border-box` and make the prefix code for it to all elements.

  2. using `scroll-behavior` to make scroll in website smooth and look good.

  3. reset the style of ul (because we will use it a lot).

  4. set `font-family` to (Cairo) for `body`.

  5. make container class to make sure my element will be in grid design and have the same padding and margin in all screen size, and make sure that element height will not be less than 100px.

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

Header have the logo & navigation links to sections in website.

1. first we make header `position` relative to make it take all width of screen without interferes property of our container (padding , margin).

2. then i create a box-shadow to make header look like navigation bar (stander design).

3. after that i make the container be flex to make elements inside it get to next to each other, and make it wrap for mobile screen (not in media query).

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

  I make a logo as a because it just text without any image on it, so we can edit that a to make it look as we want, and clickable to go to link (same home page).

1. using `text-decoration` to erase all anchor default design.

```
.header .container .logo {
    text-decoration: none;
    ...
     }
```

2. make it flex to set height and make the text center (vertical & horizontal), in mobile screen this element will have 50px of `height` and 100% of `width`, to make header be vertical in small screen (768px).

```
.header .container .logo {
   ...
    display: flex;
    justify-content: center;
    align-items: center;
}
```

- Links:

  This links will be the navigator tools to go to web sections with just one click.

1. I make `ul` flex to make links inside it line up horizontal, in mobile screen i make this element have `margin` auto to make it center when it have full width.

2. the `a` inside item of `ul` have 72px of height to change the background color when user hover on it, and it flex to center the text inside it like logo, on small screen i change the (`padding` , `font-size` , `height`) to make look more good in small screen using media query.

3. give this links a `transition` to make animation when user hover on it.

4. using `::before` to make a line that have `width:0` and when user hover the link it will increase to `width:100%` in `0.3s`.

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
