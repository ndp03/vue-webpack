<template>
    <div class="image-grid-container">
        <div class="image-grid-container__grid">    
            <div class="image-grid-container__cell" v-for="imgUrl in images" :style="{ backgroundImage: 'url(' + imgUrl + ')' }" v-on:click="focusImg(imgUrl, $event)"  >
            </div>
        </div>
        <div class="image-focus--overlay" v-if="showFocus" v-on:click="closeImg($event)"  >
            <div class="image-focus__wrapper" :style=" { backgroundImage : 'url(' + focusImgUrl + ')' }" >
            </div>
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
                images : arr,
                focusImgUrl : "",
                showFocus : false
            };
        },
        methods: {
            focusImg: function(url, event) {
                this.focusImgUrl = url;
                this.showFocus = true;
            }
            ,
            closeImg: function(event) {
                console.log(event.target);
                if (event.target.className === "image-focus--overlay") {
                    this.showFocus = false;
                }

            }
        }
    }

</script>

<style>
    .image-grid-container__grid { 
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
    .image-grid-container__cell:nth-child(1) { background-position: 50%;}
    .image-focus--overlay { border: solid 1px greenyellow; position: fixed; top: 0; left: 0; right: 0; display: flex; z-index: 100000; height: 100%; justify-content:center;}
    .image-focus__wrapper { position: relative; top: 100px; border: dotted 3px indigo; height: 600px; width: 800px; align-items: stretch; background-size: cover; background-repeat: no-repeat; }
</style>