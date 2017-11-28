<template>
    <div class="container public-container">
        <MainNav></MainNav>
        <HeroSlider></HeroSlider>
        <img-grid></img-grid>
    </div>
</template>

<script>
import MainNav from './MainNav';
import HeroSlider from './HeroSlider';
import ImgGrid from './ImageGrid';

export default {
  name: 'Public',
  //props: ['displayName', 'pictureUrl'],
  components: { MainNav, HeroSlider, ImgGrid },
  mounted: function () {
    //window.jQuery('[data-toggle="hideseek"]').off().hideseek()
  }
}
</script>

<style>
    .public-container { background-color: white; }
</style>
