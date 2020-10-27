<template>
<div class="products">
  <section class="about-breadcrum">
  <div class="breadcrum-bg">
    <div class="container py-4">
      <h2>Products</h2>
      <p><a href="index.html">Home</a> &nbsp; / &nbsp; Products</p>
    </div>
  </div>
</section>
   <div class="col-mlg-12 col-md-12">

      <section class="bg-light">
        <div class="container">
          <div class="col-lg-8 offset-lg-2 col-md-12 text-center">
         <div class="_about py-5  m-auto">
           <h1>Products</h1>
           <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam ex velit officiis corrupti. Repudiandae nam error quas quos amet</p>


         </div>

       </div>
      <div class="footer_parts">

      <div class="row prodcuts__section">
      <div class="col-lg-6">
        <div class="left_about">
          <img src="/pro1.jpg" width="100%">
        </div>
      </div>
       <div class="col-lg-6">
         <div class="right_about mt-3">
           <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit.</h3>
           <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam ex velit officiis corrupti. Repudiandae nam error quas quos amet, rem recusandae officia molestias perferendis quasi voluptas at, excepturi, adipisci eius!</p>
           <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci dolorum quam ea molestiae delectus fuga minus modi laudantium, aut ratione.</p>

           <div class="btn btn-primary know_more">Know More</div>
         </div>

       </div>

      </div>




<hr>
  <div class="row prodcuts__section">

  <div class="col-lg-6">
        <div class="left_about">
          <img src="/pro2.jpg" width="100%">
        </div>
      </div>

       <div class="col-lg-6">
         <div class="right_about mt-3">
           <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit.</h3>
           <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam ex velit officiis corrupti. Repudiandae nam error quas quos amet, rem recusandae officia molestias perferendis quasi voluptas at, excepturi, adipisci eius!</p>
           <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci dolorum quam ea molestiae delectus fuga minus modi laudantium, aut ratione.</p>

           <div class="btn btn-primary know_more">Know More</div>
         </div>

       </div>



      </div>


<hr>
  <div class="row prodcuts__section">

  <div class="col-lg-6">
        <div class="left_about">
          <img src="/pro3.jpg" width="100%">
        </div>
      </div>

       <div class="col-lg-6">
         <div class="right_about mt-3">
           <h3>Lorem ipsum dolor sit amet consectetur adipisicing elit.</h3>
           <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam ex velit officiis corrupti. Repudiandae nam error quas quos amet, rem recusandae officia molestias perferendis quasi voluptas at, excepturi, adipisci eius!</p>
           <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci dolorum quam ea molestiae delectus fuga minus modi laudantium, aut ratione.</p>

           <div class="btn btn-primary know_more">Know More</div>
         </div>

       </div>



      </div>

      </div>
        </div>
      </section>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style scoped>

.prodcuts__section{
  padding: 50px 0px;
}
.left_about{

display: flex;
justify-content: center;
}
.left_about img {
    border-radius: 10px;
    box-sizing: border-box;
    box-shadow: 0px 0px 20px 5px #CCC;

    object-fit: cover;

}
  .about-breadcrum .breadcrum-bg {
    background-size: cover;
    background-image: linear-gradient(to right, #010101, #00000026) , url(/team/bead_crum.jpg);
    background-repeat: no-repeat;

        background-position: center;
    color: #FFF;

    }
    .know_more {
    padding: 10px 30px;
    color: #FFF;
    font-size: 16px;
    text-transform: capitalize;
    font-weight: 600;
    transition: 0.3s ease-in;
    border: 2px solid #ff5b83;
    background: #ff5b83;
    margin-top: 0px;
    margin-bottom: 10px;
}
.right_about h3{
  padding: 10px 0px;
  font-size: 25px;
}
.right_about p{
  padding: 10px 0px;
  font-size: 15px;
}
@media (max-width:567px)
{
._about h1{
  font-size: 25px;
}
}
</style>


