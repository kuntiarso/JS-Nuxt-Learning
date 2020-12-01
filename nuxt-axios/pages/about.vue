<template>
  <div class="container">
    <h1>About Page</h1>
    <p>This ABOUT page is made by Kuntiarso</p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "About by Kun",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "This page is about mr Kuntiarso trying to learn Nuxt.js"
        }
      ]
    };
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
