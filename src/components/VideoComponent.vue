<template>
  <div class="container">
    <img class="container-img" src="@/assets/vueart.png" alt="vue tutorial" />
    <div class="container-info">
      <img
        class="container-info-profile"
        src="@/assets/profile.jpg"
        alt="profile image"
      />
      <div>
        <p class="container-title">Best Vue.js tutorial</p>
        <p class="container-small-title">Peter ISKANDER</p>
        <p class="container-small-title">2M views. 1 hour ago</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "VideoComponent",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">


@mixin removePaddingMargin {
  padding: 0;
  margin: 0;
}

$container-width: 350;

$image-width: calc($container-width - 20);
$profile-width: calc($container-width / 10);
.container {
  width: #{$container-width}px;
  margin: 10px;
  &-img {
    width: #{$image-width}px;
    object-fit: cover;
    margin: 5px;
  }
  &-info {
    display: flex;
    margin: 5px;
    gap: 10px;
    &-profile {
      width: #{$profile-width}px;
      height: #{$profile-width}px;
      object-fit: contain;
      border-radius: 50%;
    }
  }
  &-title {
    @include removePaddingMargin();
    font-family: "Roboto", "Arial", sans-serif;
    font-size: 1.4rem;
    color: #030303;
    margin-bottom: 5px;
  }
  &-small-title {
    @include removePaddingMargin();
    font-family: "Roboto", "Arial", sans-serif;
    font-size: 0.7rem;
    color: #606060;
    margin: 2px 0;
  }
}
</style>
