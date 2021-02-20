<template>
  <div id="app">
    <h1 class="header-color">{{ name }} by {{ author }}</h1>

    <div v-for="eachArticle in articles" v-bind:key="eachArticle.id">
      {{ eachArticle }}
      <ArticleCard v-bind:eachArticle="eachArticle" />
    </div>
  </div>
</template>

<script>
import ArticleCard from "./components/ArticleCard";
import Test from "./components/Test";

export default {
  name: "App",

  component: {
    ArticleCard,
    Test,
  },

  data() {
    return {
      name: "article1",
      author: "author1",
      articles: [
        {
          id: 1,
          name: "article1",
          author: "author1",
        },
        {
          id: 2,
          name: "article2",
          author: "author2",
        },
        {
          id: 3,
          name: "article3",
          author: "author3",
        },
      ],
    };
  },
};
</script>

<style>
.header-color {
  color: red;
}
</style>