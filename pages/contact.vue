<template>
<div>
  <section class="about-breadcrum">
  <div class="breadcrum-bg">
    <div class="container py-4">
      <h2>Contact Us</h2>
      <p><a href="index.html">Home</a> &nbsp; / &nbsp; contact</p>
    </div>
  </div>
</section>
    <div class="container fomr_wraper">
 <section class="w3l-contact-2 py-5" id="contact">
    <div class="contact-infubd section-gap py-lg-5 py-md-4">
        <div class="container">
            <div class="contact-grids d-grid">
                <div class="contact-left">
                    <h4>Leave us a Message</h4>
                    <h6>For more info or inquiry about our products project, and pricing please feel free to get in
                        touch with
                        us.</h6>
                    <div class="hours">
                        <h6 class="info mt-3">Email:</h6>
                        <p> <a href="mailto:info@example.com">
                            info@example.com</a></p>
                        <h6 class="info mt-3">Address:</h6>
                        <p> Corporate Office, #32841 block, #221DRS Lorem Street, UK.</p>
                        <h6 class="info mt-3">Contact:</h6>
                        <p class="margin-top"><a href="tel:+(121-345-6789">+121-345-6789</a></p>
                    </div>
                </div>
                <div class="contact-right">
                    <form action="https://sendmail.w3layouts.com/submitForm" method="post" class="signin-form">
                        <div class="input-grids">
                            <input type="text" name="w3lName" id="w3lName" placeholder="Your Name*" class="contact-input">
                            <input type="email" name="w3lSender" id="w3lSender" placeholder="Your Email*" class="contact-input" required="">
                            <input type="text" name="w3lSubect" id="w3lSubect" placeholder="Subject*" class="contact-input">
                        </div>
                        <div class="form-input">
                            <textarea name="w3lMessage" id="w3lMessage" placeholder="Type your message here*" required=""></textarea>
                        </div>
                        <button class="btn btn-secondary btn-theme2 submit">Send Message</button>
                    </form>
                </div>

            </div>
        </div>
</div></section>
    </div>
</div>
</template>

<script>
export default {

}
</script>

<style>
.w3l-contact-2 .contact-grids {
    grid-template-columns: 1fr 1fr;
    grid-gap: 30px;
}
.d-grid {
    display: grid;
}
.w3l-contact-2 .contact-left {
    padding-right: 28px;
}

.w3l-contact-2 .contact-left h4 {
    font-size: 36px;
    line-height: 42px;

    margin-bottom: 20px;
    font-weight: 700;
}

.w3l-contact-2 .contact-left h6 {
    font-size: 18px;
    line-height: 28px;

}
.w3l-contact-2 .contact-right {
    padding-left: 28px;
}
.w3l-contact-2 .contact-grids input, .w3l-contact-2 .contact-grids textarea {
    width: 100%;
    color: var(--text-color);
    background: #fff;
    font-size: 16px;
    font-weight: normal;
    font-style: normal;
    border: none;
    font-family: inherit;
    padding: 15px;
    border: none;
    border: 1px solid #ddd;
    outline: none;
    border-radius: 0px;
    margin-bottom: 16px;
    border-radius: 4px;
}
.w3l-contact-2 .hours p a {
    font-size: 18px;
    color: #585858;
}
.w3l-contact-2 .contact-left h6.info {
    font-size: 20px;
    line-height: 28px;
    color: #000;
}
.btn-theme2 {
    padding: 10px 30px;
    color: #FFF;
    font-size: 16px;
    text-transform: capitalize;
    font-weight: 600;
    transition: 0.3s ease-in;
    border: 2px solid #ff5b83;
    background: #ff5b83;
}

.fomr_wraper{

 display: flex;
 justify-content: center;
 align-items: center;
 width: 100%;


}
.forms{

      border: 1px solid #ccc;
      padding: 35px 25px 50px;
      border-radius:10px;
      background-color: rgb(251, 251, 251);
      width: 100%;
      margin-top: 35px;

}
  .about-breadcrum .breadcrum-bg {
    background-size: cover;
    background-image: linear-gradient(to right, #010101, #00000026) , url(/team/bead_crum.jpg);
    background-repeat: no-repeat;

        background-position: center;
    color: #FFF;

    }

@media only screen and (max-width:567px) {
.w3l-contact-2 .contact-grids {
    grid-template-columns:1fr;
    grid-gap: 30px;
}
.w3l-contact-2 .contact-right {
    padding-left:0px;
}
.w3l-contact-2 .contact-left h4 {
    font-size: 30px;
}
}
</style>
