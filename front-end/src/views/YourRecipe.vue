<template>
<section class="image-gallery">
  <div class="image" v-for="item in items" :key="item.id">
    <div class="empty"></div>
    <img :src="item.path" />
    <h2>{{item.title}}</h2>
    <h3>Ingredients</h3>
    <p>{{item.ingredients}}</p>
    <h3>Instructions</h3>
    <p>{{item.description}}</p>
  </div>
</section>
</template>

<script>
// @ is an alias to /src
import axios from 'axios';
export default {
  name: 'YourRecipe',
  data() {
    return {
      items: [],
    }
  },
  created() {
    this.getItems();
  },
  methods: {
    async getItems() {
      try {
        let response = await axios.get("/api/items");
        this.items = response.data;
        return true;
      } catch (error) {
        console.log(error);
      }
    },
  }
}
</script>

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
  font-size: 25px;
}

h3 {
  font-size: 15px;
}

/* Masonry */
*,
*:before,
*:after {
  box-sizing: inherit;
}

.image-gallery {
  column-gap: 5px;
}

.empty {
  margin-bottom: 15%;
}

.image {
  margin: 1 1 1.5em;
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
