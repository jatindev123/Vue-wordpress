<template>
<div class="slider-info banner-view bg bg2" data-selector=".bg.bg2">
            <div class="banner-info">
              <div class="container">
                <div class="banner-info-bg mx-auto text-center">
                  <h5>Check Out Our Latests Tips &amp; Tricks </h5>
                 <a class="btn btn-secondary btn-theme2 mt-md-5 mt-4" href="#">Read More</a>
                </div>
              </div>
            </div>
          </div>
</template>

<script>
export default {
  name:'BannerHeader'

}
</script>

<style>

 .banner-view {
    background: url(/team/header.jpg) no-repeat center;
    background-size: cover;
    min-height: 700px;
    position: relative;
    z-index: 0;
    display: grid;
    align-items: center;
}
 .banner-info-bg {
    max-width: 700px;
}
 .banner-view:before {
    content: "";
    background: rgba(7, 10, 12, 0.45);
    position: absolute;
    top: 0;
    min-height: 100%;
    left: 0;
    right: 0;
    z-index: -1;
}
 .banner-info-bg h5 {
    font-size: 60px;
    line-height: 68px;
    font-weight: 600;
    color: #FFF;
}
@media (max-width:567px)
{
.banner-info-bg h5 {
    font-size: 30px;
    line-height: 36px;
}
.banner-view {

    min-height: 300px;

}
.heading p{
  font-size: 12px;
}
}
</style>

