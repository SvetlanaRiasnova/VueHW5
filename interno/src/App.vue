<template>
  <div id="app">
    <HomePage />
    <BlogPage />
    <BlogDetailsPage />
  </div>
</template>

<script>
import HomePage from "./components/pages/HomePage.vue";
import BlogDetailsPage from "./components/pages/BlogDetailsPage.vue";
import BlogPage from "./components/pages/BlogPage.vue";

export default {
  name: "App",
  components: {
    HomePage,
    BlogPage,
    BlogDetailsPage,
  },
};
</script>

<style lang="scss">
#app {
  $familyTitle: "DM Serif Display", serif;
  $familyText: "Jost", sans-serif;
  $headerColor: #292f36;
  $textColor: #4d5053;

  @mixin flexCenter {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  @mixin logoImage {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  @mixin logoText {
    font-family: $familyTitle;
    font-size: 40px;
    font-weight: 400;
    color: $headerColor;
  }

  @mixin h2Style {
    font-family: $familyTitle;
    color: $headerColor;
    font-size: 50px;
    font-weight: 400;
    line-height: 62.5px;
  }

  * {
    box-sizing: border-box;
    font-family: $familyText;
    color: $textColor;
  }
}
.container {
  width: 1200px;
  margin: 0 auto;
}
</style>
