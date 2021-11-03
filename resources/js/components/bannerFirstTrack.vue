<template>
    <!-- <div class="banner"> -->
        <div class="banner">
            <div class="banner__wrap">
                <h2 class="banner__title banner__item">Загрузи свой <br/> первый трек</h2>
                <p class="banner__text banner__item">Твои будущие фанаты ждут! Жми <br/> на кнопку «добавить трек» и переходи<br/>к продвижению прямо сейчас.</p>
                <btnPrimary sign="Добавить трек" showIcon="true" @btnPrimaryClick="buttonClick"/>
            </div>
            <div class="banner__img"></div>
        </div>
        <!-- <div class="banner__right">
            <img src="/img/bannerPhoto.png" alt="Веселый человек с гитарой">
        </div>     -->
</template>

<script>
import btnPrimary from "./btnPrimary";

export default {
    name: "bannerFirstTrack.vue",
    components: {
        btnPrimary
    },
    methods: {
        buttonClick() {
            this.$emit("btnPrimaryClick");
        }
    }
}

</script>

<style scoped>
    .banner {
        background-color: #FFFFFF;
        width: 972px;
        max-width: 100%;
        height: 250px;
        border-radius: 24px;
        box-shadow: 0px 11px 39px -14px #D1D5DD;
        position: relative;
        overflow: hidden;

    }

    .banner__wrap {
        padding: 29px 33px; 
        position: relative;
        z-index: 1;
    }

    .banner__img {
        background-image: url(../img/bannerPhoto.png), url(../img/bannerBG.png);
        background-repeat: no-repeat;
        background-position-y: bottom;
        background-position-x: calc(100% - 30px), calc(100% - 190px);
        position: absolute;
        top: 0;
        width:100%;
        height: 100%;
        z-index: 0;
    }

    @media only screen and (max-width: 1030px)  {
        .banner__img {
            background-image: url(../img/bannerPhotoTablet.png), url(../img/bannerBG.png);
            background-position-x: right;  
        }  
    }

    @media only screen and (max-width: 660px)  {
        .banner {
            height: 500px; 
            width: 310px;
            margin: 0 auto;
        }  

        .banner__img {
            background-image: url(../img/bannerPhotoMobile.png), url(../img/bannerBGMobile.png);
            top: auto;
            bottom: 0;
            background-position-y: 140px, 175px;  
        }    

    }
    
    .banner__item {
        margin-bottom: 20px;
    }

    .banner__title {
        font-size: 24px;
        font-weight: 600;
        line-height: 110%;
    }

    .banner__text {
        font-size: 13px;
        line-height: 135%;        
    }
</style>
