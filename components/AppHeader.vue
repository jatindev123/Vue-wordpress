<template>
<div>
   <nav class="navbar navbar-expand-lg navbar-dark bg-primary static-top">
    <div class="container">

      <b-navbar-brand to="/" class="nav-heading">
      Logo
    </b-navbar-brand>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarResponsive">

         <ul class="navbar-nav ml-auto">
      <li class="nav-item" v-for="post of service" :key="post.id">
        <NuxtLink :to="post.url" class="nav-link active-link">{{ post.title }}</NuxtLink>

      </li>
    </ul>


      </div>
    </div>
  </nav>

</div>
</template>

<script>
import axios from "axios";
export default {
name:'AppHeader',
data(){
  return{
    service:[]
  }
},

async created(){
  const config={
    header:{
      'Accepts':'appication/json'
    }
  }
  try {
    const res = await axios.get('https://jake.pswebdev.com.au/index.php?rest_route=/wp-api-menus/v2/menu-locations/main-menu' ,config);
    this.service = res.data;
   }catch(err){
}
}



}
</script>
<style scoped>

.navbar-dark {
    background-color: #ff7500f5 !important;
}
.navbar-dark .navbar-nav .nav-link {

    color: #FFF;
}
</style>

