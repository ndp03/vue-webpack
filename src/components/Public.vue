<template>
    <div class="container public-container">
        <MainNav></MainNav>
        <HeroSlider></HeroSlider>
    </div>
</template>

<script>
import MainNav from './MainNav';
import HeroSlider from './HeroSlider';

export default {
  name: 'Public',
  //props: ['displayName', 'pictureUrl'],
  components: { MainNav, HeroSlider },
  mounted: function () {
    //window.jQuery('[data-toggle="hideseek"]').off().hideseek()
  }
}
</script>

<style>
    .public-container { background-color: white; }
</style>
