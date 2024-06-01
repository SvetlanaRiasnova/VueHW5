<template>
  <div>
    <HeaderComponent />
    <div class="banner__blog_details"></div>
    <section class="articles__list">
      <BlogDetailsComponent></BlogDetailsComponent>
    </section>
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "../HeaderComponent.vue";
import BlogDetailsComponent from "../BlogDetailsComponent.vue";
import FooterComponent from "../FooterComponent.vue";

export default {
  name: "BlogDetailsPage",
  components: {
    HeaderComponent,
    BlogDetailsComponent,
    FooterComponent,
  },

  data() {},
  methods: {},
  mounted() {},
};
</script>

<style lang="scss">
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
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: $familyText;
  color: $textColor;
}

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.banner__blog_details {
  background-image: url("../../assets/img/Banner_DetailsBlog.png");
  min-height: 356px;
}

.blog__page {
  display: flex;
  padding-top: 197px;
  gap: 52px;
  &_wrapper {
    width: 800px;
  }
  &_article {
    padding-bottom: 21px;
    &-title {
      padding-bottom: 21px;
      color: $headerColor;
      font-family: $familyTitle;
      font-size: 50px;
      font-weight: 400;
      line-height: 125%;
      text-align: left;
    }
    &-img {
      border-radius: 50px;
    }
    &-text {
      padding-bottom: 38px;
      font-size: 22px;
      font-weight: 400;
      line-height: 150%;
      text-align: left;
    }
    &-info {
      padding-top: 46px;
      padding-bottom: 48px;
      display: flex;
      justify-content: space-between;
      font-size: 16px;
      font-weight: 400;
      line-height: 150%;
      text-align: left;
      text-transform: capitalize;
    }
    &-link {
      padding-right: 60px;
    }
    &-quote {
      @include flexCenter;
      width: 799px;
      height: 267px;
      flex-direction: column;
      padding: 53px 227px 53px 227px;
      border-radius: 50px;
      background: #f4f0ec;
    }
    &-simbol {
      color: #cda274;
      font-family: $familyTitle;
      font-style: italic;
      font-size: 200px;
      font-weight: 400;
      line-height: 125%;
      text-align: center;
      padding: 0;
    }
    &-quote-text {
      width: 345px;
      color: #cda274;
      font-family: $familyTitle;
      font-style: italic;
      font-size: 25px;
      font-weight: 400;
      line-height: 125%;
      text-align: center;
      margin-top: -100px;
    }
    &-ordered-description {
      padding-left: 30px;
    }
  }
}
.blog__tags {
  width: 345px;
  &_header {
    color: $headerColor;
    font-family: $familyTitle;
    font-size: 25px;
    font-weight: 400;
    line-height: 125%;
    text-align: left;
    padding-bottom: 24px;
  }
  &_btns {
    display: flex;
    flex-wrap: wrap;
    row-gap: 11px;
  }
  &_btn {
    padding: 9px 30px 9px 30px;
    border: none;
    border-radius: 10px;
    background: rgb(244, 240, 236);
    color: #000000;
    margin: 0px 10px;
    &:focus {
      background: #292f36;
      color: #ffffff;
    }
  }
}
ol li::marker {
  color: #cda274;
  font-family: $familyTitle;
  padding-left: 14px;
  font-size: 20px;
  font-weight: 400;
  line-height: 125%;
  text-align: left;
}
</style>
