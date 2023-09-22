---
title: Responsive Wannabe
author: Francesco Carrara
---

### ASSIGNMENT: MEDIA QUERY

given a non responsive full html css document we have to add media queries:

- **standard size** (or windows-size) bigger than 1160px
- **tablet size** between 480 and 768 px
- **mobile size** below 480px

- **BONUS** between 768 and 1160 px

---

### [html]()

before modifing the css document we have to add this command in the header to make it screen responsive

    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

---

## [css]()

##### [standard size]()

- standard size was already responsive so no nees to change it
  <br />

---

##### [tablet size]()

for tablet size we have to modify the outer container dimension, so it won`t appear any sidebar, using the @media propriety

```css
@media screen and (max-width: 768px) {
  .container {
    width: 100%;
  }
}
```

- writing a propriety inside of the graphs allows to override a certain class when the condition inside the rounds brackets is verified.
- in this case we modified the dimensions of the outer container, so its screen will adapt to the dimensions of the page whithout creating an horizontal scrollbar

---

##### [mobile size]()

in mobile size we kept the same proprieties of tablet size, modifing mainly the display of the images and adjusting the dimensions of flexed items _minor changes in background color and the dimensions of some inner items_

```css
@media screen and (max-width: 480px) {
  .row {
    flex-direction: column;
    align-items: center;
  }

  /* 		specific changes  		*/

  .var .column {
    width: 100%;
  }
}
```

- first propriety allows to modify the direction of the layout direction of the items inside of the page
- second propriety allows to modify the width of some items to make them fit inside of the outer container
- made also specific changes to the padding and the margin of the page

<br>

---

##### BONUS

we copied the propriety of the tablet size for screen with width between 768 and 1160 px to avoid the horizontal scrollbar

```css
@media screen and (max-width: 1160px) {
  .container {
    width: 100%;
  }
}
```

> _when you`re changing a propriety in css, his last value shadows all previous ones risking to modifing undesired items. To overcome this problem, keep your propriety ordered from generic to specific. in this case this propriety was put BEFORE tablet@media_

<br>
