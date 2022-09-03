<template>
  <div class="hello">
    <header class="masthead" style="background-image: url('../../static/assets/img/home-bg.jpg')">
      <div class="container position-relative px-4 px-lg-5">
        <div class="row gx-4 gx-lg-5 justify-content-center">
          <div class="col-md-10 col-lg-8 col-xl-7">
            <div class="site-heading">
              <h1>Clean Blog</h1>
              <span class="subheading">A Blog Theme by Start Bootstrap</span>
            </div>
          </div>
        </div>
      </div>
    </header>
    <!-- Main Content-->
    <div class="container px-4 px-lg-5">
      <div class="row gx-4 gx-lg-5 justify-content-center">
        <div class="col-md-6 col-lg-6 col-xl-6" v-for="product in products.data" :key="product.id">
          <!-- Post preview-->
          <div class="post-preview">
            <img v-if="product.photo" :src="`http://127.0.0.1:8000/upload/product/${product.photo}`"
              class="profile-user-img img-fluid img-circle" style="height:400px; width:100%;" />
            <router-link :to="{ name: 'PostDetails', params: { id: product.id } }">
              <h6 class="post-title">{{ product.name }}
              </h6>
            </router-link>
            <span class="post-subtitle">{{ product.description | truncate(100, '...') }}</span>
            <p class="post-meta">
              Posted by
              <a href="#!">Admin</a>
              on {{ product.created_at }}
            </p>

          </div>
          <!-- Divider-->
          <hr class="my-4" />
        </div>
        <!-- Pager-->
        <div class="d-flex justify-content-end mb-4"><a class="btn btn-primary text-uppercase" href="#!">Older Posts
            →</a></div>

      </div>
    </div>

  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'Home',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App',
      products: {},
    }
  },
  methods: {
    loadProducts() {
      let APP_URL = 'http://127.0.0.1:8000/api';

      axios.get(APP_URL + "/product").then(({ data }) => (this.products = data.data));
    },
  },
  mounted() {

  },
  created() {
    this.loadProducts();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
