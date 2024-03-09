# Ekko Website Template
In this website I am gonna share everything about my life. Books Iam reading, Games Iam Playing, Stories and Events, it is like a portfolio but it something little personal.

>[!tip]
>This a clone project to practice my skill in CSS & HTML.
>This project will be updated with js when i finish learn it.

**I will emplane everything i code it to make this repository as recourse guide to check it later.**

## Let's Start 💥

### Prepare Started file for project.

- Create My HTML file and type my head content that it have:

    1. [Normalize](https://necolas.github.io/normalize.css/) CSS File: to make all content get default property value.
    2. Font Awesome CDN: to use icon from [font-awesome](https://fontawesome.com/) website.
    3. [Google Font](https://fonts.google.com/): using Cairo font style for all element in website.
    4. Main CSS File: the main css style fo whole project.
    *(Whole work in this file)*

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
