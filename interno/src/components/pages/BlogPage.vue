<template>
  <div>
    <HeaderComponent />
    <section class="banner">
      <div class="banner__info">
        <h1 class="banner__info_header">Articles & News</h1>
        <div class="banner__info_breadcrump">Home / Blog</div>
      </div>
    </section>
    <section class="latest__article container">
      <h2 class="latest__article_title">Latest Post</h2>
      <div class="latest__article_wrapper">
        <div class="latest__article_image">
          <img
            class="latest__article_image"
            src="..//../assets/img/last_article.png"
            alt="article picture"
          />
        </div>
        <div class="latest__article_content">
          <h3 class="latest__article_content-header">
            Low Cost Latest Invented Interior Designing Ideas
          </h3>
          <p class="latest__article_content-text">
            Lorem ipsum dolor sit amet, adipiscing Aliquam eu sem vitae turpis
            dignissim maximus.posuere in.Contrary to popular belief.
          </p>
          <p class="latest__article_content-text">
            Lorem Ipsum is not simply random text. It has roots in a piece of
            classica.
          </p>
          <div class="latest__article_bottom-wrap">
            <div class="latest__article_date">22 December,2022</div>
            <button class="latest__article_btn">
              <svg
                width="70.000000"
                height="70.000000"
                viewBox="0 0 70 70"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
              >
                <desc>Created with Pixso.</desc>
                <defs />
                <circle
                  id="Ellipse"
                  cx="34.000122"
                  cy="35.000000"
                  r="35.000000"
                  fill="#F4F0EC"
                  fill-opacity="1.000000"
                />
                <path
                  id="Vector"
                  d="M31 44L39 35L31 26"
                  stroke="#292F36"
                  stroke-opacity="1.000000"
                  stroke-width="2.000000"
                  stroke-linejoin="round"
                  stroke-linecap="round"
                />
              </svg>
            </button>
          </div>
        </div>
      </div>
    </section>
    <section class="blog container">
      <h2 class="blog__header blogs__title">Articles & News</h2>
      <ArticleComponent :quantity="6"></ArticleComponent>

      <div class="count__page">
        <div class="count__page_wrap">
          <a href="#" class="count__page_number">
            <p class="count__page-number_value">01</p>
          </a>
          <a href="#" class="count__page_number">
            <p class="count__page-number_value">02</p>
          </a>
          <a href="#" class="count__page_number">
            <p class="count__page-number_value">03</p>
          </a>
          <a href="#">
            <svg
              class="count__page_svg"
              width="54.000000"
              height="54.000000"
              viewBox="0 0 70 70"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
            >
              <circle
                id="Ellipse"
                cx="34.000122"
                cy="35.000000"
                r="35.000000"
                fill="#F4F0EC"
                fill-opacity="1.000000"
              />
              <path
                id="Vector"
                d="M31 44L39 35L31 26"
                stroke="#292F36"
                stroke-opacity="1.000000"
                stroke-width="2.000000"
                stroke-linejoin="round"
                stroke-linecap="round"
              />
            </svg>
          </a>
        </div>
      </div>
    </section>
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "../HeaderComponent.vue";
import ArticleComponent from "../ArticleComponent.vue";
import FooterComponent from "../FooterComponent.vue";
export default {
  name: "BlogPage",
  components: {
    HeaderComponent,
    ArticleComponent,
    FooterComponent,
  },
  data() {
    return {};
  },
  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped>
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

.banner {
  background-image: url("..//../assets/img/Banner.png");
  min-height: 356px;
  @include flexCenter;
  align-items: flex-end;

  &__info {
    text-align: center;
    background-color: #fff;
    padding: 41px;
    border-radius: 37px 37px 0px 0px;

    &_header {
      @include h2Style;
      text-align: left;
    }

    &_breadcrump {
      font-size: 22px;
      font-weight: 400;
      line-height: 33px;
    }
  }
}

.latest__article {
  padding-top: 150px;

  &_wrapper {
    border: 1px solid #e7e7e7;
    display: flex;
    gap: 62px;
    padding: 22px;
    border-radius: 62px;
    align-items: center;
  }

  &_title {
    margin-bottom: 30px;
    @include h2Style;
  }

  &_image {
    max-width: 569px;
    border-radius: 50px;
  }

  &_content {
    min-height: 478px;
    padding-top: 51px;

    &-header {
      font-family: $familyTitle;
      color: $headerColor;
      font-size: 25px;
    }

    &-text {
      padding-top: 22px;
      margin-bottom: 41px;
      font-size: 22px;
      font-style: normal;
      font-weight: 400;
      line-height: 150%;
    }
  }

  &_bottom-wrap {
    padding-top: 30px;
    width: 489px;
    @include flexCenter;
    flex-wrap: nowrap;
    justify-content: space-between;
  }

  &_btn {
    width: 52px;
    background-color: inherit;
    border: none;

    &svg circle {
      width: 52px;
      cursor: pointer;
    }
  }
}
//blog
.blog {
  margin-top: 96px;

  &__header {
    font-family: $familyTitle;
    color: $headerColor;
    font-size: 50px;
    font-weight: 400;
    line-height: 125%;
    text-align: center;
  }

  &__description {
    width: 810px;
    margin: 0 auto;
    font-size: 22px;
    font-weight: 400;
    line-height: 150%;
    text-align: center;
  }

  &__articles {
    padding-top: 52px;
    display: flex;
    flex-direction: row;
    justify-content: center;
    gap: 27px;

    &_back {
      padding: 21px;
      width: 382px;
      @include flexCenter;
      flex-direction: column;
      box-sizing: border-box;
      border: 1px solid rgb(231, 231, 231);
      border-radius: 62px;
      box-shadow: 0px 10px 30px 0px rgba(255, 255, 255, 0.25);

      &:hover {
        background: #f4f0ec;
      }
    }
  }

  &__articles_header {
    position: absolute;
    @include flexCenter;
    margin: 0;
    width: 129px;
    height: 41px;
    transform: translate(10%, -160%);
    font-size: 16px;
    font-weight: 400;
    line-height: 150%;
    text-transform: capitalize;
    background-color: #ffffff;
    border-radius: 8px 8px 8px 0px;
  }

  &__title {
    margin: 0;
    padding-top: 21px;
    padding-right: 60px;
    width: 80%;
    font-family: $familyTitle;
    color: $headerColor;
    font-size: 25px;
    font-weight: 400;
    line-height: 125%;
    text-align: left;
  }

  &__articles_bottom {
    padding-top: 30px;
    width: 340px;
    @include flexCenter;
    flex-wrap: nowrap;
    justify-content: space-between;
  }

  &__articles_btn {
    background-color: inherit;
    border: none;

    & svg circle:hover {
      fill: #ffffff;
    }
  }
}
.blogs__title {
  text-align: left;
}

.blog_page {
  flex-wrap: wrap;
}

.count__page {
  margin-top: 51px;
  padding-bottom: 200px;
  display: flex;
  justify-content: center;

  &_wrap {
    display: flex;
    gap: 20px;
  }

  &_number {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: nowrap;
    border: 1px #cda274 solid;
    width: 52px;
    height: 52px;
    border-radius: 52px;
    text-decoration: none;

    &_value {
      font-size: 16px;
      font-style: normal;
      font-weight: 500;
      line-height: 24px;
      text-transform: capitalize;
    }

    &:hover {
      background: #f4f0ec;
      border: none;
      width: 54px;
      height: 54px;
    }
  }

  & circle#Elips:hover {
    fill: #f4f0ec;

    & circle {
      stroke: none;
    }
  }
}

.footer__blog {
  padding-top: 0;
}
</style>
