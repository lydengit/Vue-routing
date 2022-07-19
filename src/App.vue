<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name: 'about' }">About</router-link> |
    <router-link :to="{ name: 'contact' }">Contact</router-link> |
    <router-link :to="{ name: 'jobs' }">Jobs</router-link>
  </nav>
  <div>
    <button @click="goBack">Back</button>
    <button @click="forward">Forward</button>
    <button @click="redirect">Redirect</button>
  </div>
  <router-view></router-view>
</template>
<script>
export default {
  methods: {
    goBack() {
      this.$router.go(-1);
    },
    forward() {
      this.$router.go(1);
    },
    redirect(){
      this.$router.push({
        name: 'home'
      })
    }
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
