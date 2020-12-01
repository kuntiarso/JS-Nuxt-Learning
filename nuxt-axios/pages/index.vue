<template>
  <div class="container">
    <h1>Home Page</h1>
    <p>This HOME page is made by Kuntiarso</p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "Home by Kun",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "This page is created for a landing page"
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
