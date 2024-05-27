# Step by Step Guide on how to create the Portfolio Website

## 1. Initial Setup

Create the `index.html` , `style.css` and `app.js` files.
Create folder `img` and add the appropriate images in it.

## 2. Index.html initial setup

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Portfolio</title>
  </head>

  <body>
    <!-- Link the JS -->
    <script src="./app.js"></script>
  </body>
</html>
```

Link the css file

```html
<!-- Link the CSS -->
<link rel="stylesheet" href="./style.css" />
```

Add the google fonts

```html
<!-- GOOGLE FONTS -->
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap"
  rel="stylesheet"
/>
```

## 3. Building the first section

Adding the `container` and the first section `intoduction`

```html
<div class="container">
  <!-- INTRODUCTION -->
  <div class="intro">
    <div class="salute">
      <div class="saluteTextContainer">
        <h1 class="saluteText">Hi</h1>
      </div>
      <div class="saluteImgContainer">
        <img src="./img/person.png" alt="Person Image" class="saluteImg" />
      </div>
    </div>
    <div class="nameContainer">
      <h2 class="name">I'm John</h2>
    </div>
    <div class="jobTitleContainer dark">
      <h2 class="jobTitle">a Web Developer</h2>
    </div>
    <div class="jobTitleContainer purple ">
      <h2 class="jobTitle">and Designer</h2>
    </div>
  </div>
</div>
```

## 4. Styling the introduction section
