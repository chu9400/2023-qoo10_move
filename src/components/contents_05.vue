<script setup>
    import {contData05} from "../constants/index.js";
</script>

<template>
    <section id="contents__05" class="contents__05__wrap">
        <div class="contents__05__inner">

            <div class="ct__img__05_00">    
                <picture>
                    <!-- <source media="(max-width: 800px)" :srcset="contData05[7]"> -->
                    <img :src="contData05[0]" alt="콘텐츠 이미지 00">
                </picture>
            </div>

            <div class="ct__img__05_01">    
                <picture>
                    <img :src="contData05[1]" alt="콘텐츠 이미지 01">
                </picture>
            </div>

            <div class="ct__img__05_02">    
                <picture>
                    <img :src="contData05[2]" alt="콘텐츠 이미지 02">
                </picture>
            </div>

            <div class="ct__img__05_03">    
                <picture>
                    <img :src="contData05[3]" alt="콘텐츠 이미지 03">
                </picture>
            </div>

            <div class="ct__img__05_04">    
                <picture>
                    <img :src="contData05[4]" alt="콘텐츠 이미지 04">
                </picture>
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
            this.animation05();
        },
        methods: {
            animation05() {

                gsap.from(".ct__img__05_00", {
                    autoAlpha: 0,
                    y: 100,
                    scrollTrigger: {
                    trigger: ".ct__img__05_00",
                    start: "top bottom",
                    end: "+=500px",
                    scrub: 1,
                    }
                });

                gsap.from(".ct__img__05_01", {
                    autoAlpha: 0,
                    y: 100,
                    scrollTrigger: {
                    trigger: ".ct__img__05_01",
                    start: "top bottom",
                    end: "+=500px",                    
                    scrub: 1,
                    }
                });

                gsap.from(".ct__img__05_02", {
                    autoAlpha: 0,
                    y: 100,
                    scrollTrigger: {
                    trigger: ".ct__img__05_02",
                    start: "top bottom",
                    end: "+=500px",
                    scrub: 1,
                    }
                });

                gsap.from(".ct__img__05_03", {
                    autoAlpha: 0,
                    x: -100,
                    scrollTrigger: {
                    trigger: ".ct__img__05_03",
                    start: "top bottom",
                    end: "+=500px",
                    scrub: 1,
                    }
                });

                gsap.from(".ct__img__05_04", {
                    autoAlpha: 0,
                    x: 100,
                    scrollTrigger: {
                    trigger: ".ct__img__05_04",
                    start: "top bottom",
                    end: "+=500px",
                    scrub: 1,
                    }
                });

            }
        }
    }
    
</script>

<style lang="scss">

@import "../assets/scss/vars.scss";

.contents__05__wrap {
    width: 100%;
    background: url("@/assets/img/cont05/contents_05_bg.jpg") no-repeat center / cover;
    overflow: hidden;
}

.contents__05__inner {
    width: 100%;
    position: relative;
    padding-top: 70%;

    @media(max-width: 800px) {
        padding-top: 293%;
    }
    
    .ct__img__05_00 {      
                            // $width, $left, $margin-top, $border-radius
        @include cont01-img-style(18%, 62%, 10%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(40%, 13%, 177%, 20px);
        }
    }
    
    .ct__img__05_01 {      
        @include cont01-img-style(18%, 20%, 14%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(40%, 30%, 27%, 20px);
        }

    }
    
    .ct__img__05_02 {      
        @include cont01-img-style(18%, 41%, 27%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(40%, 47%, 116%, 20px);
        }

    }
    
    .ct__img__05_03 {      
        @include cont01-img-style(22%, 5.2%, 21.5%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(55%, -9%, 38%, 20px);
        }

    }
    
    .ct__img__05_04 {      
        @include cont01-img-style(26%, 67%, 29%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(54%, 38.3%, 205%, 20px);
        }

    }




}
</style>