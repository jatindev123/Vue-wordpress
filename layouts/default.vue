<template>
  <div id="container">
    <AppHeader />
    <div class="main">
    <Nuxt />
    </div>
    <AppFooter />
  </div>
</template>
<script>
import AppHeader from '../components/AppHeader'
import AppFooter from '../components/AppFooter'

export default {

  components:{
    AppHeader,
    AppFooter


  }

}
</script>
<style>
#container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

.main {
  flex: 1;
}
</style>
