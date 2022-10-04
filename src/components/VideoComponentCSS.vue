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
  name: "VideoComponentCSS",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
p {
  padding: 0;
  margin: 0;
}

.container {
  width: 350px;
  margin: 10px;
}
.container-img {
  width: 330px;
  object-fit: cover;
  margin: 5px;
}
.container-info {
  display: flex;
  margin: 5px;
  gap: 10px;
}
.container-info-profile {
  width: 35px;
  height: 35px;
  object-fit: contain;
  border-radius: 50%;
}
.container-title {
  font-family: "Roboto", "Arial", sans-serif;
  font-size: 1.4rem;
  color: #030303;
  margin-bottom: 5px;
}
.container-small-title {
  font-family: "Roboto", "Arial", sans-serif;
  font-size: 0.7rem;
  color: #606060;
  margin: 2px 0;
}
</style>
