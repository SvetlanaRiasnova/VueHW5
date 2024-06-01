<template>
  <section class="banner">
    <div class="banner__info">
      <h1 class="banner__info_header">{{ bunnerHeader }}</h1>
      <div class="banner__info_breadcrump">Home / Blog</div>
    </div>
  </section>
</template>

<script>
export default {
  name: "BaseBanner",
  props: {
    bunnerHeader: String,
    imagePath: String,
  },
  data() {},
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
  box-sizing: border-box;
  font-family: $familyText;
  color: $textColor;
}
.banner {
  // background-image: url('${imagePath}');
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
</style>
