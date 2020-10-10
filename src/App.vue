<template>
  <div id="app">
    <div class="mt-3">
      <b-button-group>
        <b-button variant="outline-success"
          ><router-link to="/" exact-tag="li">Home</router-link></b-button
        >
        <b-button variant="outline-success">
          <router-link to="/country" exact-tag="li">Country</router-link>
        </b-button>
        <b-button variant="outline-success">
          <router-link to="/about" exact-tag="li">About</router-link>
        </b-button>
      </b-button-group>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
export default {};
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
.router-link-exact-active {
  color: #28a745;
  font-weight: bold;
}
</style>
