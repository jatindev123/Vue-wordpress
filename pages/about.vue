<template>
  <div class="about__us">

<section class="about-breadcrum">
  <div class="breadcrum-bg">
    <div class="container py-4">
      <h2>About Us</h2>
      <p><a href="index.html">Home</a> &nbsp; / &nbsp; About</p>
    </div>
  </div>
</section>

    <div class="about__section">

    <div class="col-lg-12 col-md-12">


      <section class="about__us py-5">
      <div class="container">
       <div class="heading text-center mx-auto">
           <h1 class="py-2" v-if="about.title">{{about.title.rendered}}</h1>
            <p  v-if="about.content" v-html="about.content.rendered" />



          </div>
      <div class="footer_parts py-3">
      <div class="row">
      <div class="col-lg-6">
        <div class="left_about">
          <img v-if="about.acf" :src="about.acf.image" width="100%">
        </div>
      </div>

        <div class="col-lg-6">
        <div class="right_about">
        <h3 class="py-2" v-if="about.acf">{{about.acf.why_choose_us}}</h3>
        <p class="py-2" v-if="about.acf" v-html="about.acf.description" />


        </div>
        </div>

      </div>
      </div>
        </div>
      </section>
    </div>
    </div>

    <!-- Team Start -->



    <!-- Team End -->




    </div>

</template>

<script>
import axios from "axios";
export default {
   name:'Aboutpage',

data(){
  return{
    about:[]
  }
},

async created(){
  const config={
    header:{
      'Accepts':'appication/json'
    }
  }
  try {
    const res = await axios.get('https://jake.pswebdev.com.au/index.php?rest_route=/wp/v2/pages/56' ,config);
    this.about = res.data;

   }catch(err){
}
}

}
</script>

<style scoped>

    .about__section{
         background: #f6f6f6;
    }
    ul.choose__us{
      margin: 0;
      padding: 0;
      box-sizing: border-box;

    }
    .choose__us li{
      list-style-type:none;
      margin-bottom: 10px;
      margin-left: 0px;

    }
     .choose__us li img{
       width: 20px;
       height: 20px;
       margin-right: 10px;
     }
    .right_about{
      background-color: transparent;
    }
    .team_img img{
      border-radius:10px;
      display: block;
    transition: transform 0.3s linear;

    }
     .team_img img:hover{
      transition: transform 0.3s linear;
    }
    .team_details h3{
      font-weight: 700;
      padding: 20px 0px 0px 0px;


    }
     .team_details p{
      font-weight: 600;
      margin-bottom: 0px;
       color: #ff5b83;

    }
    .team_img img {
    height: 350px;
    object-fit: cover;
    width: 100%;
}
    .team_section{
      padding: 75px 0px;
          background-color: #efefef;

    }
    .about-breadcrum .breadcrum-bg {
    background-size: cover;
    background-image: linear-gradient(to right, #010101, #00000026) , url(/team/bead_crum.jpg);
    background-repeat: no-repeat;

        background-position: center;
    color: #FFF;

    }
  .heading {
    max-width: 750px;
}

</style>
