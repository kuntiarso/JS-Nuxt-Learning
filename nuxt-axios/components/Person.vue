<template>
  <div class="person">
    <p>name : {{ firstName }} {{ lastName }}</p>
    <p>country: {{ country }}</p>
  </div>
</template>

<script>
export default {
  name: "person",
  props: ["firstName", "lastName", "country", "id"]
};
</script>

<style>
.person {
  padding: 1rem;
  border: 1px dotted #ccc;
  margin: 1rem 0;
}
</style>
