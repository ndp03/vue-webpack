<template>
    <div class="image-grid-container">
        <div class="image-grid-container__cell" v-for="imgUrl in images" :style="{ backgroundImage: 'url(' + imgUrl + ')' }" >
            <!--<img class="image-grid-container__img" :src="imgUrl" alt="" />-->
        </div>
    </div>
</template>

<script> 
    export default {    
        data : function() {
            var arr = [];
            for (var i = 1; i < 9; i++) {
                arr.push("https://s3-ap-southeast-2.amazonaws.com/labbit01/landscapes/00" + i + ".jpg");
            }

            return {
                images : arr
            };
        }
    }

</script>

<style>
    .image-grid-container { 
        border: solid 2px yellow; 
        display: grid; 
        justify-content: left ; 
        align-items: left ; 
        /*grid-template-columns: 20% 20% 20% 20% 20%;*/
        grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
        /*grid-template-rows: 20% 20% 20% 20% 20%;*/
        background-image: repeating-linear-gradient(-45deg, pink, pink 10px, hotpink 10px, hotpink 12px, pink 12px);
    }
    .image-grid-container__cell { height: 100px; border : solid 2px red; background-size: cover; background-repeat: no-repeat;}
    .image-grid-container__img { width: 100px; height: 100px; }
</style>