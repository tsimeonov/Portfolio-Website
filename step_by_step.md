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

## 6. Style the project section

```css
.projects {
  display: flex;
  flex-direction: column;
  gap: 30vh;
  padding: 0 100px;
}

.projectsTitle {
  font-size: 10vw;
  color: #333;
}

.project {
  display: flex;
  align-items: center;
  gap: 100px;
  height: 100vh;
  overflow: hidden;
}

/* Find the even elements and reverse their position */
.project:nth-child(2n) {
  flex-direction: row-reverse;
}

.phone {
  flex: 1;
  width: 300px;
  height: 600px;
  position: relative;
}

.phoneScreen {
  width: 264px;
  height: 567px;
  position: absolute;
  top: 17px;
  left: 18px;
  border-radius: 28px;
  overflow: scroll;
}

/* Remove the scrollbar */
.phoneScreen::-webkit-scrollbar {
  display: none;
}

.phoneApp {
  width: 100%;
}

.projectDetail {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.projectTitle {
  font-size: 7vw;
  color: #555;
}

.projectDesc {
  font-size: 20px;
  color: #555;
  text-align: justify;
  line-height: 40px;
  margin: 40px 0;
}

.projectButton {
  padding: 10px 20px;
  background-color: transparent;
  border: 2px solid #555;
  color: #555;
  cursor: pointer;
  position: relative;
  overflow: hidden;
}

.projectButton::after {
  content: "View Demo";
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: -100%;
  transition: 1s all;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #555;
  color: #222;
}

.projectButton:hover.projectButton::after {
  transform: translateX(100%);
}

.laptop {
  width: 600px;
  height: 379px;
  flex: 1;
  position: relative;
}

.laptopScreen {
  width: 451px;
  height: 283px;
  position: absolute;
  top: 18px;
  left: 68px;
  overflow: scroll;
}

.laptopApp {
  width: 100%;
}

/* Remove the scrollbar */
.laptopScreen::-webkit-scrollbar {
  display: none;
}
```

## 7. Build the Github section

```html
<!-- GITHUB -->
<div class="githubContainer">
  <h1 class="githubTitle">Want to see all projects?</h1>
  <div class="githubChart">
    <div class="dates">
      <span>Jan</span>
      <span>Feb</span>
      <span>Mar</span>
      <span>Apr</span>
      <span>May</span>
      <span>Jun</span>
      <span>Jul</span>
      <span>Aug</span>
      <span>Sep</span>
      <span>Oct</span>
      <span>Nov</span>
      <span>Dec</span>
    </div>
    <div class="boxContainer"></div>
    <h1 class="githubTitle">ON GITHUB</h1>
  </div>
  <div class="githubSm">
    <a href="#">
      <img src="./img/github.png" alt="" />
    </a>
    <h2>Find me on Github</h2>
  </div>
</div>
```

## 8. Style the Github section

```css
.githubContainer {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
}

.githubTitle {
  font-size: 100px;
  color: #333;
}

.githubChart {
  width: 820px;
  text-align: center;
}

.dates {
  padding: 10px;
  color: #555;
  font-size: 12px;
  display: flex;
  justify-content: space-between;
}

.boxContainer {
  display: flex;
  flex-wrap: wrap;
  gap: 5px;
}

.box {
  width: 15px;
  height: 15px;
  background-color: #171c25;
  border-radius: 2px;
  cursor: pointer;
  transition: 2s all ease;
}

.active:nth-child(4n) {
  background-color: #195b2c;
}

.githubChart:hover .active:nth-child(2n + 1) {
  background-color: #195b2c;
}

.githubChart:hover .active:nth-child(2n) {
  background-color: #063f24;
}

.githubSm {
  display: none;
}
```

## 9. Add interactivity to the github section

```js
for (let i = 0; i < 365; i++) {
  const list = [
    0, 1, 2, 3, 41, 42, 43, 44, 82, 83, 123, 124, 125, 126, 164, 165, 166, 167,
    205, 206, 246, 247, 287, 288, 5, 6, 46, 47, 87, 88, 128, 129, 169, 170, 210,
    211, 251, 252, 292, 293, 8, 9, 14, 15, 49, 50, 51, 90, 91, 92, 131, 132,
    133, 134, 172, 173, 213, 214, 254, 255, 295, 296, 175, 176, 217, 177, 218,
    259, 55, 56, 96, 97, 137, 138, 178, 179, 219, 220, 260, 261, 217, 218, 259,
    260, 261, 301, 302, 17, 18, 19, 58, 59, 60, 61, 99, 100, 102, 103, 140, 141,
    144, 181, 182, 185, 222, 223, 225, 226, 263, 264, 265, 266, 304, 305, 306,
    24, 25, 65, 66, 67, 106, 107, 108, 147, 148, 149, 150, 188, 189, 229, 230,
    270, 271, 311, 312, 67, 108, 149, 150, 191, 232, 192, 233, 274, 234, 275,
    316, 194, 235, 276, 154, 195, 236, 73, 114, 155, 33, 34, 74, 75, 115, 116,
    156, 157, 197, 198, 238, 239, 279, 280, 320, 321, 36, 37, 38, 39, 77, 78,
    79, 80, 118, 119, 159, 160, 161, 162, 200, 201, 202, 203, 241, 242, 282,
    283, 284, 285, 323, 324, 325, 326,
  ];

  const el = document.createElement("div");
  el.classList = list.includes(i) ? "box active" : "box";
  boxContainer.appendChild(el);
}
```
