<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Navbar</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
          <a class="nav-link" href="#">Features</a>
          <a class="nav-link" href="#">Pricing</a>
          <a class="nav-link disabled" aria-disabled="true">Disabled</a>
        </div>
      </div>
    </div>
  </nav>

  <router-link to="/">홈페이지</router-link>
  <router-link to="/list">리스트페이지</router-link>
  <!-- <router-link to="/detail">상세페이지</router-link> -->

  <div class="mt-4">
    <router-view :blogData="blogDatas"></router-view>
  </div>

  <!-- <List :blogData="blogDatas" /> -->
</template>

<script>
import blog from "./assets/blog";
// import List from "./components/List.vue";

export default {
  name: "App",
  data() {
    return {
      blogDatas: blog,
    };
  },
  components: {
    // List: List,
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
}
</style>
