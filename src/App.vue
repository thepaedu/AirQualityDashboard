<template>
  <div>
    <Login v-if="!isLoggedIn" @login-success="handleLoginSuccess" />
    <Dashboard v-else />
  </div>
</template>

<script>
import Login from './components/Login.vue';
import Dashboard from './components/Dashboard.vue';

export default {
  components: { Login, Dashboard },
  data() {
    return {
      isLoggedIn: false,
    };
  },
  methods: {
    handleLoginSuccess() {
      this.isLoggedIn = true;
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
  background-color: #f8f9fa;
  color: #333333;
  margin: 0;
}

body #app {
  display: block;
}

div#app {
  width: 100%;
}

#app {
  padding: 0 0rem;
  max-width: 100%;
}

html,
body {
  overflow-x: hidden; /* Verhindert horizontales Scrollen */
}

.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.footer {
  margin-top: auto;
}
</style>
