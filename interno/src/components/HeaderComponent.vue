<template>
  <header class="header container">
    <div class="header__logo">
      <svg
        width="34.000000"
        height="35.000000"
        viewBox="0 0 34 35"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        xmlns:xlink="http://www.w3.org/1999/xlink"
      >
        <desc>Created with Pixso.</desc>
        <defs />
        <path
          id="Logo"
          d="M0 34L13.45 34L13.45 24.49C13.45 22.48 15.08 20.85 17.1 20.85C19.11 20.85 20.74 22.48 20.74 24.49L20.74 34L33.99 34L33.99 0C15.22 0 0 15.22 0 34Z"
          fill="#CDA274"
          fill-opacity="1.000000"
          fill-rule="nonzero"
        />
      </svg>
      <span class="header__logo_text">Interno</span>
    </div>
    <nav class="header__menu">
      <a href="#" class="header__nav_item">Home</a>
      <a href="#" class="header__nav_item">Project</a>
      <a href="#" class="header__nav_item">Blog</a>
    </nav>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",

  data() {},

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
  box-sizing: border-box;
  font-family: $familyText;
  color: $textColor;
}
//header
.header {
  height: 151px;
  display: flex;
  justify-content: space-between;
  align-items: center;

  &__logo {
    display: flex;
    align-items: center;
    gap: 10px;
  }
  &__logo_text {
    font-family: $familyTitle;
    font-size: 40px;
    font-weight: 400;
    color: $headerColor;
  }
  &__menu {
    display: flex;
    flex-direction: row;
    gap: 40px;
  }
  &__nav_item {
    text-decoration: none;
    color: $headerColor;
    font-size: 20px;
    font-weight: 400;
    line-height: 125%;
  }
}
</style>
