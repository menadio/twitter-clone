<template>
  <div id="app">
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
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
