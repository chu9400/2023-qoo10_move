<script setup>
    import {contData02} from "../constants/index.js";
</script>

<template>
    <section id="contents__02" class="contents__02__wrap">
        <div class="contents__02__inner">
            <div class="ct__img__02_01 reveal">
                <figure>
                    <img :src="contData02[0]" alt="콘텐츠 이미지 01">
                    <figcaption>콘텐츠 이미지 01</figcaption>
                </figure>
            </div>

            <div class="ct__img__02_02 reveal">
                <figure>
                    <img :src="contData02[1]" alt="콘텐츠 이미지 02">
                    <figcaption>콘텐츠 이미지 02</figcaption>
                </figure>
            </div>

            <div class="ct__img__02_03 reveal">
                <figure>
                    <img :src="contData02[2]" alt="콘텐츠 이미지 03">
                    <figcaption>콘텐츠 이미지 03</figcaption>
                </figure>
            </div>

        </div>
    </section>
</template>

<script>
    import gsap from "gsap";
    import ScrollTrigger from "gsap/ScrollTrigger";
    gsap.registerPlugin(ScrollTrigger);

    export default {
        mounted : function() {
            this.animation02();
        },
        methods: {
            animation02() {
                
                gsap.from(".ct__img__02_01", {
                    autoAlpha: 0,
                    y: 100,
                    scrollTrigger: {
                    trigger: ".ct__img__02_03",
                    start: "top bottom",
                    end: "+=600px",
                    markers: false,
                    id:"111",
                    scrub: 1,
                    }
                });

                gsap.from(".ct__img__02_02", {
                    autoAlpha: 0,
                    y: 100,
                    scrollTrigger: {
                    trigger: ".ct__img__02_02",
                    start: "top bottom",
                    end: "+=500px",
                    markers: false,
                    id:"222",
                    scrub: 1,
                    }
                });

                gsap.from(".ct__img__02_03", {
                    autoAlpha: 0,
                    y: 100,
                    scrollTrigger: {
                    trigger: ".ct__img__02_03",
                    start: "top bottom",
                    end: "+=200px",
                    markers: false,
                    id:"333",
                    scrub: 1,
                    }
                });
               
            }
        }
    }
    
</script>

<style lang="scss">

@import "../assets/scss/vars.scss";

.contents__02__wrap {
    width: 100%;
    background: url("@/assets/img/contents_02_bg.jpg") no-repeat center / cover;
    /* overflow: hidden; */
}

.contents__02__inner {
    width: 100%;
    position: relative;
    padding-top: 87%;

    @media(max-width: 800px) {
        padding-top: 200%;
    }
    
    .ct__img__02_01 {      
        @include cont01-img-style(30%, 7%, 14%, 20px);// $width, $left, $margin-top, $border-radius
        box-shadow: 0 30px 70px #5f5f5f66;
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(60%, 20%, 41%, 20px);
            z-index: 1;
        }
    }

    
     .ct__img__02_02 {
        @include cont01-img-style(33%, 47%, 24.5%, 0px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(52%, -4%, 101.5%, 0px);
            z-index: 2;
        }
    }


    .ct__img__02_03 {
        @include cont01-img-style(20%, 85%, 10%, 15px);
        position: absolute;
        top: 0;
        
        @media(max-width: 800px) {
            @include cont01-img-style(40%, 70%, 15%, 15px);
            z-index: 0;
        }
    }



}
</style>