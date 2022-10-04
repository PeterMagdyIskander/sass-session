<template>
  <div id="app">
    <h1 class="titlecss">TITLE CSS</h1>
    <h1 class="titlescss">TITLE SCSS</h1>
    <p>ad</p>

    <!-- <p class="header-title">Centered</p>  -->
    <!-- <div class="videos-container">
      <videoComponentSCSS />
      <videoComponentSCSS />
      <videoComponentSCSS />
      <videoComponentSCSS />

      <videoComponentCSS />
      <videoComponentCSS />
      <videoComponentCSS />
      <videoComponentCSS />
    </div>
 -->

    <div class="nesting">
      <div class="nesting square"></div>
      <div class="square"></div>
      <div class="nesting-square"></div>
    </div>

  </div>
</template>

<script>
import videoComponentSCSS from "./components/VideoComponent.vue";
import videoComponentCSS from "./components/VideoComponentCSS.vue";

export default {
  name: "App",
  components: {
    videoComponentSCSS,
    videoComponentCSS,
  },
};
</script>

<style lang="scss">

@use 'sass' as *;





//SASS Variables
$color-header: red;

//CSS Variables
:root {
  --color-heading: red;
}

@mixin createHeader($margin, $title, $margin-top-bottom, $margin-left-right) {
  .header-#{$title} {
    width: fit-content;
    #{ $margin}: #{$margin-top-bottom}px #{$margin-left-right};
  }
}
@mixin removePaddingMargin() {
  padding: 0;
  margin: 0;
}

p {
  @include removePaddingMargin();
}

%displayFlex{
  display: flex;
  justify-content: center;
  gap: 10px;
}



%same-font {

  font: {
    family: Arial, "Helvetica Neue", Helvetica, sans-serif;
    size: 1.7rem;
    weight: 800;
  }


  margin: {
    right: 10px;
    bottom: 50px;
  }


}




#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
.videos {
  &-container {
    display: flex;
    flex-wrap: wrap;
  }
}
@mixin displayFlex($flex-direction-column, $justify-content){
    display: flex;
    @if $flex-direction-column{
        flex-direction: column;
    }
    justify-content: $justify-content;
}

.nesting {
  width: 100%;
  height: 700px;
  margin: 0 auto;
  @extend %displayFlex;

  & .square {
    @include removePaddingMargin();
    width: 100px;
    height: 100px;
    background-color: red;
  }
  .square {
    @include removePaddingMargin();
    width: 100px;
    height: 100px;
    background-color: Green;
    /* @extend %same-font; */
  }
  &-square {
    @include removePaddingMargin();
    width: 100px;
    height: 100px;
    background-color: Blue;
    /* @extend %same-font; */
    /* &:hover{
      background-color: red;

    } */
  }
}





.titlecss {
  color: var(--color-heading);
  --color-heading: #00ff00;
}

.titlescss {
  color: $color-header;
  $color: #00ff00;
}

@include createHeader("margin", "title", 0, "auto");
//https://docs.google.com/presentation/d/1JxNZP8GnOcsmoE8ogyWeUaDoaX00W4U_j6_KD0A7pjI/edit?usp=sharing
</style>
