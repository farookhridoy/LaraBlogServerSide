<template>
    <div>
        <header class="masthead" style="background-image: url('../../static/assets/img/about-bg.jpg')">
            <div class="container position-relative px-4 px-lg-5">
                <div class="row gx-4 gx-lg-5 justify-content-center">
                    <div class="col-md-10 col-lg-8 col-xl-7">
                        <div class="page-heading">
                            <h1>Post Details</h1>
                            <span class="subheading">{{ product.name }}</span>
                        </div>
                    </div>
                </div>
            </div>
        </header>
        <!-- Main Content-->
        <main class="mb-4">
            <div class="container px-4 px-lg-5">
                <div class="row gx-4 gx-lg-5 justify-content-center">
                    <div class="col-md-10 col-lg-8 col-xl-7">
                        <img v-if="product.photo" :src="`http://127.0.0.1:8000/upload/product/${product.photo}`"
                            class="profile-user-img img-fluid img-circle" style="height:400px; width:100%;" />
                        <p>{{ product.description }}</p>
                    </div>
                </div>
            </div>
        </main>
    </div>
</template>

<script>
import axios from 'axios';
export default {
    data() {
        return {
            product: {}
        }
    },
    created() {
        let APP_URL = 'http://127.0.0.1:8000/api';
        axios.get(APP_URL + `/post/${this.$route.params.id}`).then(({ data }) => (this.product = data.data));
    },
    methods: {
    }
}
</script>