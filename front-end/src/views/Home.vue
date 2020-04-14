<template>
<div class="home">
  <div class="description">
    <h1 class="header_desc"> Welcome!</h1>
    <p> Ever wanted to keep track of your recipes online?! <br><br>
      Now you can! with Yummy Food Recipe Book</p>
    <img src="/cook1.jpg" width=40%>
  </div>
</div>
</template>

<style scoped>
.description {
  text-align: center;
  font-family: 'Comic Neue', cursive;
  font-size: 22px;
}

.header_desc {
  font-family: 'Comic Neue', cursive;
  font-size: 28px;
}

.image h2 {
  font-style: italic;
}

/* Masonry */
*,
*:before,
*:after {
  box-sizing: inherit;
}

.image-gallery {
  column-gap: 1.5em;
}

.image {
  margin: 0 0 1.5em;
  display: inline-block;
  width: 100%;
}

.image img {
  width: 100%;
}

/* Masonry on large screens */
@media only screen and (min-width: 1024px) {
  .image-gallery {
    column-count: 4;
  }
}

/* Masonry on medium-sized screens */
@media only screen and (max-width: 1023px) and (min-width: 768px) {
  .image-gallery {
    column-count: 3;
  }
}

/* Masonry on small screens */
@media only screen and (max-width: 767px) and (min-width: 540px) {
  .image-gallery {
    column-count: 2;
  }
}
</style>
