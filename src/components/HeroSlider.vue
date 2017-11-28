<template>
    <!-- === Slider ===-->
    <div class="slider-inner">
        <!--<div id="da-slider" class="da-slider" style="background-position: 400% 0%; background-image: url('static/plugins/parallax-slider/img/bg.jpg')" >-->
        <div id="da-slider" class="da-slider" style="background-position: 0% 0%; background-image: url('https://s3-ap-southeast-2.amazonaws.com/labbit01/landscapes/001.jpg'); background-size: contain;" >
        
            <div class="da-slide da-slide-toleft">
                <h2><i>CLEAN &amp; FRESH</i> <br> <i>FULLY RESPONSIVE</i> <br> <i>DESIGN</i></h2>
                <p><i>Lorem ipsum dolor amet</i> <br> <i>tempor incididunt ut</i> <br> <i>veniam omnis </i></p>
                <div class="da-img"><img class="img-responsive" src="static/plugins/parallax-slider/img/1.png" alt=""></div>
            </div>
            <div class="da-slide da-slide-toleft">
                <h2><i>RESPONSIVE VIDEO</i> <br> <i>SUPPORT AND</i> <br> <i>MANY MORE</i></h2>
                <p><i>Lorem ipsum dolor amet</i> <br> <i>tempor incididunt ut</i></p>
                <div class="da-img">
                    <iframe src="http://player.vimeo.com/video/47911018" webkitallowfullscreen="" mozallowfullscreen="" allowfullscreen="" width="530"
                        height="300" frameborder="0"></iframe>
                </div>
            </div>
            <div class="da-slide da-slide-fromright da-slide-current">
                <h2><i>USING BEST WEB</i> <br> <i>SOLUTIONS WITH</i> <br> <i>HTML5/CSS3</i></h2>
                <p><i>Lorem ipsum dolor amet</i> <br> <i>tempor incididunt ut</i> <br> <i>veniam omnis </i></p>
                <div class="da-img"><img src="static/plugins/parallax-slide/img/html5andcss3.png" alt="image01"></div>
            </div>
            <div class="da-arrows">
                <span class="da-arrows-prev"></span>
                <span class="da-arrows-next"></span>
            </div>
            <nav class="da-dots"><span class=""></span><span class=""></span><span class="da-dots-current"></span></nav>
        </div>
    </div>
    <!-- === End Slider ===-->
</template>

<script>
    export default {
        name: 'HeroSlider',
        //props: ['displayName', 'pictureUrl'],
        //components: { SidebarMenu },
        mounted: function () {
            $('#da-slider').cslider({
                current: 0,
                // index of current slide

                bgincrement: 50,
                // increment the background position 
                // (parallax effect) when sliding

                autoplay: false,
                // slideshow on / off

                interval: 4000
                // time between transitions
            });
        }
    }

</script>

<style>

</style>