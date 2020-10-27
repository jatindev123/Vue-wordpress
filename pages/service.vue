<template>
<div class="">


<section class="about-breadcrum">
  <div class="breadcrum-bg">
    <div class="container py-4">
      <h2>Service What We Offer </h2>
      <p><a href="index.html">Home</a> &nbsp; / &nbsp; Service</p>
    </div>
  </div>
</section>


<section class="w3l-services2" id="stats">
			<div class="features-with-17_sur py-5">
				   <div class="container py-md-3">
					<div class="heading text-center mx-auto">
						<h3 class="head" v-if="service.title">{{service.title.rendered}}</h3>
						<p class="my-3 head"  v-if="service.excerpt"
            v-html="service.excerpt.rendered" ></p>
					  </div>




				     <div class="row pt-5 mt-3">
						<div class="col-lg-5 features-with-17-left_sur">
              <span v-if="service.content" v-html="service.content.rendered" />


							<div class="stats-1">
							<div class="stats-1-left">
                	<h4 v-if="service.acf">{{service.acf.work.clients}}</h4>
								<h6>Clients</h6>
							</div>
							<div class="stats-1-left">
								<h4 v-if="service.acf">{{service.acf.work.awards}}</h4>
								<h6>Awards</h6>
							</div>
							<div class="stats-1-left">
								<h4 v-if="service.acf">{{service.acf.work.projects}}</h4>
								<h6>Projects</h6>
							</div>
						</div>
						</div>
						<div class="col-lg-7 my-lg-0 my-5 align-self-center features-with-17-right_sur">

		<div class="features-with-17-right-tp_sur">
								<div class="features-with-17-left1">
									<span class="fa fa-laptop s4"></span>
								</div>
								<div class="features-with-17-left2">
									<h6 v-if="service.acf"><a href="#url">{{service.acf.seo_solution}}</a></h6>
									  <p v-if="service.acf" v-html="service.acf.seo_solution_description" />
								</div>
							</div>

							<div class="features-with-17-right-tp_sur">
								<div class="features-with-17-left1">
										<span class="fa fa-database s5"></span>
								</div>
								<div class="features-with-17-left2">
											<h6 v-if="service.acf"><a href="#url">{{service.acf.social_media}}</a></h6>
										  <p v-if="service.acf" v-html="service.acf.social_media_description" />
								</div>
							</div>

							<div class="features-with-17-right-tp_sur">
								<div class="features-with-17-left1">
									<span class="fa fa-lock s3"></span>
								</div>
								<div class="features-with-17-left2">
										<h6 v-if="service.acf"><a href="#url">{{service.acf.branding_identity}}</a></h6>
										  <p v-if="service.acf" v-html="service.acf.seo_solution_description" />
								</div>
							</div>

							<div class="features-with-17-right-tp_sur">
								<div class="features-with-17-left1">
										<span class="fa fa-codepen s2"></span>
								</div>
								<div class="features-with-17-left2">
											<h6 v-if="service.acf"><a href="#url">{{service.acf.content_marketing}}</a></h6>
                        <p v-if="service.acf" v-html="service.acf.content_marketing_description" />
								</div>
							</div>



						</div>
					</div>
				</div>
			</div>
		</section>






</div>
</template>

<script>
import axios from "axios";
export default {
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
    const res = await axios.get('https://jake.pswebdev.com.au/index.php?rest_route=/wp/v2/pages/69' ,config);
    this.service = res.data;


}catch(err){
 console.log(err)
}





}
}
</script>

<style scoped>
  .about-breadcrum .breadcrum-bg {
    background-size: cover;
    background-image: linear-gradient(to right, #010101, #00000026) , url(/team/bead_crum.jpg);
    background-repeat: no-repeat;

        background-position: center;
    color: #FFF;

    }


.w3l-services2 .features-with-17_sur{

    background: rgba(7, 10, 12, 0.45);
    background: rgba(23, 68, 158, 0.6);
    background: linear-gradient(45deg, #17449e, #000000cf);

}
.w3l-services2 .features-with-17-right_sur {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 30px;
}
.w3l-services2 .features-with-17-right-tp_sur {
    padding: 40px;
    background: rgba(46, 93, 235, 0.33);
    transition: 0.3s ease;
    -moz-transition: 0.3s ease;
    -ms-transition: 0.3s ease;
    -o-transition: 0.3s ease;
    border-radius: 4px;
}


.w3l-services2 .features-with-17-left1 span {
    font-size: 32px;
    color: #FFF
}
.w3l-services2 .features-with-17-left2 h6 a {
    color: #fff;
    text-decoration: none;
    font-weight: bold;
}

.heading {
    max-width: 750px;
    color: #FFF;
}
.heading h3 {
    font-size: 36px;
    line-height: 42px;
    color: #FFF;
    font-weight: 600;
}

.w3l-services2 h4.lft-head {
    font-size: 38px;
    color: #fff;
    line-height: 46px;
    font-weight: 600;
}

.w3l-services2 p {
    color: #d0d0d0;
    margin-top: 10px;
    font-size: 16px;
    line-height: 24px;
}
.w3l-services2 .stats-1 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 10px;
    margin-top: 50px;
}
.w3l-services2 .stats-1 h4 {
    font-size: 36px;
    color: #fff;
    font-weight: 600;
    margin-bottom: 6px;
}

.w3l-services2 .stats-1 h6 {
    font-size: 18px;
    color: #fff;
    margin-top: 0px;
}

.left_side_service{
  background-color: rgb(37, 36, 36);
  height: 200px;
  border-radius: 5px;


}
.btn-primary{
  background-color: #000;
border-radius: 0px;
border:1px solid #000;

}
.service__item{
  margin-bottom: 20px;
  background-color: cadetblue;
  border-radius: 5px;
}
.service__desc{
margin: auto;

}
.lft-head {
    color: #FFF;
}
.col-lg-5.features-with-17-left_sur p {
    color: #FFF;
}
@media only screen and (max-width:567px) {
.w3l-services2 .features-with-17-right_sur {
    display: grid;
    grid-template-columns:1fr;
    grid-gap: 30px;
}
.w3l-services2 h4.lft-head {
    font-size: 21px;
    color: #fff;
    font-weight: 600;
}
.w3l-services2 .features-with-17-right-tp_sur {
    padding: 20px;

}
.heading h3 {
    font-size: 30px;

}
.w3l-services2 .stats-1 h4 {
    font-size: 20px;

}
}
</style>
