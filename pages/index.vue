<template>
<div>
  <BannerHeader />
  <div id="page__content">
  <div class="posts_section py-5">
          <div class="heading text-center mx-auto mb-5">
            <h3 class="">Recent posts and updates</h3>
            <p>Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nulla mollis dapibus nunc, ut rhoncus turpis sodales quis. Integer sit amet mattis quam.</p>
          </div>
        <div class="container">
          <div class="row">
                <div class="col-md-4 mb-2" v-for="post of blogpost" :key="post.id">
                  <div class="team_img">

                       <img v-if="post.acf" :src="post.acf.image" width="100%">
                  </div>
                  <div class="team_details text-left">
                    <div class="row">
                    <div class="col-lg-6 auth">{{post.status}}</div>

                    </div>
                    <h5> {{post.title.rendered}} </h5>
                    <p v-html="post.content.rendered"/>
                    <a href="#" class="read_more">Read More</a>
                  </div>
                </div>
          </div>
        </div>

  </div>
  </div>
</div>
</template>
<script>

import BannerHeader from '../components/baner_header'
import axios from "axios";
export default {

  components:{
    BannerHeader

  },
  data(){
  return{
    blogpost:[]
  }
},

async created(){
  const config={
    header:{
      'Accepts':'appication/json'
    }
  }

  try {
    const res = await axios.get('https://jake.pswebdev.com.au/index.php?rest_route=/wp/v2/posts&per_page=3' ,config);
    this.blogpost = res.data;

}
catch(err){

}
}
}
</script>


<style scoped>

html,
body {
  height: 100%;
}
#what_they_says{
  background-color: rgb(219, 219, 219);
}
.team_details{
padding: 20px;
background-color: rgb(243, 240, 240);
}
.test_details{
  padding: 20px;
background-color: rgb(255, 255, 255);
border-radius: 10px;
border: 2px solid  #ff5b83;
}
.right_about {
    background-color: #d9dddd;
    padding: 25px;
    border-radius: 10px;
}

  .heading {
    max-width: 750px;
}
.read_more{
   background-color: #ff5b83;
  font-weight: 400;
  text-decoration: none;
  cursor: pointer;
 color: #FFF;
  padding: 5px 10px;
  border-radius:2px;
  display: inline-block;

}
.team_details h5{
  font-size: 20px;
  font-weight: 600;
  padding: 15px 0px 5px 0px;
  color: #4d4d4d;
}
.team_details p{
  font-size: 15px;
  font-weight: 200;
}
.auth {
  color: #ff5b83;
  font-weight: 500;
  font-size: 15px;
  text-transform:capitalize;
}
.date{
  color: #4d4d4d;
  font-weight: 500;
   font-size: 12px;
}


.team_img_test img{
  height: 100px;
  width: 100px;
  border-radius: 50%;
  object-fit: cover;

}
.name{
  font-weight: 600;
  color: #ff5b83;
  font-size: 20px;
}
</style>



