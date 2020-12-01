<template>
  <div class="container">
    <h1>Pringles Page</h1>
    <p>This PRINGLES page is made by Kuntiarso</p>
    <Person
      v-for="p in person"
      :key="p.id"
      :id="p.id"
      :firstName="p.firstName"
      :lastName="p.lastName"
      :country="p.countryOfBirth"
    />
  </div>
</template>

<script>
import Person from "../../components/Person";

export default {
  components: {
    Person
  },
  data() {
    return {
      person: []
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json"
      }
    };

    try {
      const res = await this.$axios.$get(
        "https://kun-personapp.herokuapp.com/api/person/get-all",
        config
      );

      this.person = res;
    } catch (err) {
      console.log(err);
    }
  },
  head() {
    return {
      title: "Pringles by Kun",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "This page is created randomly by mr Kuntiarso"
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
