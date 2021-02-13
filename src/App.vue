<template>
  <div id="app" class="container mx-auto my-2 font-sans text-xl">
    @{{ user.username }} - {{ fullname }}
    <strong></strong>
  </div>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      followers: 0,
      user: {
        id: 1,
        username: "itzmena",
        firstname: "Elomena",
        lastname: "Onome",
        email: "hellodevelo@gmail.com",
        isAdmin: true,
      },
    };
  },

  computed: {
    fullname() {
      return `${this.user.firstname} ${this.user.lastname}`;
    },
  },

  methods: {
    followUser() {
      this.followers++;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
