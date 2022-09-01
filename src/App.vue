<style>
@import '../static/css/styles.css';
</style>
<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-dark" id="mainNav">
      <div class="container px-4 px-lg-5">
        <router-link to="/" class="navbar-brand">LaraBlogs</router-link>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarResponsive"
          aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
          Menu
          <i class="fas fa-bars"></i>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <ul class="navbar-nav ms-auto py-4 py-lg-0">
            <li class="nav-item">
              <router-link to="/" class="nav-link nav-link px-lg-3 py-3 py-lg-4">Home</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/about" class="nav-link nav-link px-lg-3 py-3 py-lg-4">About</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/post" class="nav-link nav-link px-lg-3 py-3 py-lg-4">All Post</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/contact" class="nav-link nav-link px-lg-3 py-3 py-lg-4">Contact Us</router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <router-view />
    <!-- Footer-->
    <footer class="border-top">
      <div class="container px-4 px-lg-5">
        <div class="row gx-4 gx-lg-5 justify-content-center">
          <div class="col-md-10 col-lg-8 col-xl-7">
            <ul class="list-inline text-center">
              <li class="list-inline-item">
                <a href="#!">
                  <span class="fa-stack fa-lg">
                    <i class="fas fa-circle fa-stack-2x"></i>
                    <i class="fab fa-twitter fa-stack-1x fa-inverse"></i>
                  </span>
                </a>
              </li>
              <li class="list-inline-item">
                <a href="#!">
                  <span class="fa-stack fa-lg">
                    <i class="fas fa-circle fa-stack-2x"></i>
                    <i class="fab fa-facebook-f fa-stack-1x fa-inverse"></i>
                  </span>
                </a>
              </li>
              <li class="list-inline-item">
                <a href="#!">
                  <span class="fa-stack fa-lg">
                    <i class="fas fa-circle fa-stack-2x"></i>
                    <i class="fab fa-github fa-stack-1x fa-inverse"></i>
                  </span>
                </a>
              </li>
            </ul>
            <div class="small text-center text-muted fst-italic">Copyright &copy; Your Website 2022</div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>
<script>
import '../static/js/scripts.js';
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
