<template>
    <div class="container public-container">
        <MainNav></MainNav>

        <h1>Public</h1>
    </div>
</template>

<script>
import MainNav from './MainNav'

export default {
  name: 'Public',
  //props: ['displayName', 'pictureUrl'],
  components: { MainNav },
  mounted: function () {
    //window.jQuery('[data-toggle="hideseek"]').off().hideseek()
  }
}
</script>

<style>
    .public-container { background-color: white; }
</style>
