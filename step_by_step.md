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

The code for styling the `introduction` section.

```css
* {
  padding: 0;
  margin: 0;
  font-family: "Open Sans", sans-serif;
}

.container {
  background-color: #111;
  overflow: hidden;
}

.salute {
  height: 100vh;
  display: flex;
  align-items: center;
  overflow: hidden;
}

/* The saluteTextContainer is 3 times bigger than the saluteImgContainer */

.saluteTextContainer {
  flex: 3;
}

.saluteImgContainer {
  flex: 1;
}

.saluteText {
  color: #333;
  font-size: 60vw;
  cursor: default;
}

.saluteImg {
  width: 100%;
}

.nameContainer {
  height: 100vh;
  background-color: rebeccapurple;
}

.name {
  font-size: 20vw;
  color: #333;
  cursor: default;
  /* Center vertical and horizonal */
  text-align: center;
  line-height: 100vh;
}

.jobTitleContainer {
  height: 100vh;
}

.dark {
  background: url("./img/bg1.png");
}

.purple {
  background: rebeccapurple url("./img/bg2.png");
}

.jobTitle {
  font-size: 10vw;
  color: #333;
  line-height: 100vh;
  cursor: default;
}
```

## 5. Building the second section

```html
<!-- PROJECTS -->
<div class="projects">
  <div class="projects">
    <h1 class="projectTitle">Here are some of my projects</h1>
    <div class="project">
      <div class="phone">
        <img src="./img/phone.png" alt="" />
        <div class="phoneScreen">
          <img src="./img/phone1.png" alt="" class="phoneApp" />
        </div>
      </div>
      <div class="projectDetail">
        <h1 class="projectTitle">Vortex</h1>
        <p class="projectDesc">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore ut
          voluptatum voluptatem, dolorum laborum maiores, nemo incidunt facilis
          sed accusamus deleniti repellat asperiores quae nihil fugit fugiat
          quidem! Soluta nam repudiandae ut repellat consectetur alias quia
          eligendi provident dolor laborum!
        </p>
        <button class="projectButton">learn more</button>
      </div>
    </div>
    <div class="project">
      <div class="laptop">
        <img src="./img/laptop.png" alt="" />
        <div class="laptopScreen">
          <img src="./img/laptop1.png" alt="" class="phoneApp" />
        </div>
      </div>
      <div class="projectDetail">
        <h1 class="projectTitle">Studio</h1>
        <p class="projectDesc">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore ut
          voluptatum voluptatem, dolorum laborum maiores, nemo incidunt facilis
          sed accusamus deleniti repellat asperiores quae nihil fugit fugiat
          quidem! Soluta nam repudiandae ut repellat consectetur alias quia
          eligendi provident dolor laborum!
        </p>
        <button class="projectButton">learn more</button>
      </div>
    </div>
    <div class="project">
      <div class="phone">
        <img src="./img/phone.png" alt="" />
        <div class="phoneScreen">
          <img src="./img/phone1.png" alt="" class="phoneApp" />
        </div>
      </div>
      <div class="projectDetail">
        <h1 class="projectTitle">Vortex</h1>
        <p class="projectDesc">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Tempore ut
          voluptatum voluptatem, dolorum laborum maiores, nemo incidunt facilis
          sed accusamus deleniti repellat asperiores quae nihil fugit fugiat
          quidem! Soluta nam repudiandae ut repellat consectetur alias quia
          eligendi provident dolor laborum!
        </p>
        <button class="projectButton">learn more</button>
      </div>
    </div>
  </div>
</div>
```
