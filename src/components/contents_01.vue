<script setup>
    import {contData01} from "../constants/index.js";
</script>

<template>
    <section id="contents__01" class="contents__01__wrap">
        <div class="contents__01__inner">
            <div class="ct__img__01 reveal">
            <picture>
                <source media="(max-width: 800px)" :srcset="contData01[7]">
                <img :src="contData01[0]" alt="콘텐츠 이미지 01">
            </picture>
            </div>

            

            <div class="ct__img__02 reveal growBig">
                <figure>
                    <img :src="contData01[1]" alt="콘텐츠 이미지 02">
                    <figcaption>콘텐츠 이미지 02</figcaption>
                </figure>
            </div>

            <div class="ct__img__03 reveal growBig">
                <figure>
                    <img :src="contData01[2]" alt="콘텐츠 이미지 03">
                    <figcaption>콘텐츠 이미지 03</figcaption>
                </figure>
            </div>

            <div class="ct__img__04 reveal growBig">
                <figure>
                    <img :src="contData01[3]" alt="콘텐츠 이미지 04">
                    <figcaption>콘텐츠 이미지 04</figcaption>
                </figure>
            </div>

            <div class="ct__img__05 reveal growBig">
                <figure>
                    <img :src="contData01[4]" alt="콘텐츠 이미지 05">
                    <figcaption>콘텐츠 이미지 05</figcaption>
                </figure>
            </div>

            <div class="ct__img__06 reveal growBig">
                <figure>
                    <img :src="contData01[5]" alt="콘텐츠 이미지 06">
                    <figcaption>콘텐츠 이미지 06</figcaption>
                </figure>
            </div>

            <div class="ct__img__07 reveal growBig">
                <figure>
                    <img :src="contData01[6]" alt="콘텐츠 이미지 07">
                    <figcaption>콘텐츠 이미지 07</figcaption>
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
        this.animation();
    },
    methods: {
        animation() {

            gsap.from(".ct__img__01", {
                autoAlpha:0,
                y: 100,
                scrollTrigger: {
                    trigger: ".ct__img__01",
                    start : "top bottom",
                    end: "+=500px",
                    markers: false,
                    scrub:1,
                    
                }
            });


            const horizontalAni = [".ct__img__03", ".ct__img__04", ".ct__img__05", ".ct__img__06"];

            horizontalAni.forEach((elementClass) => {
                gsap.from(elementClass, {
                    autoAlpha: 0,
                    x: -50,
                    scrollTrigger: {
                    trigger: elementClass,
                    start: "top bottom",
                    end: "+=500",
                    markers: false,
                    scrub:1,
                    
                    },
                });
            });

            gsap.from(".ct__img__02", {
                autoAlpha:0,
                y: 100,
                scrollTrigger: {
                    trigger: ".ct__img__02",
                    start : "top bottom",
                    end: "+=500",
                    markers: false,
                    scrub:1,
                }
            });

            gsap.from(".ct__img__07", {
                autoAlpha:0,
                x: -200,
                scrollTrigger: {
                    trigger: ".ct__img__07",
                    start : "top bottom",
                    end: "+=500",
                    markers: false,
                    scrub:1,
                }
            });

            const growBigImg = document.querySelectorAll(".growBig");
            growBigImg.forEach( img => {
                img.addEventListener("mouseover", () => {
                    gsap.to(img, { scale: 1.015 });
                });
                img.addEventListener("mouseleave", () => {
                    gsap.to(img, { scale: 1 });
                });
            })

        }
    }
}
    
</script>

<style lang="scss">

@import "../assets/scss/vars.scss";

.contents__01__wrap {
    max-width: 1920px;
    margin: 0 auto;
    width: 100%;
    background: url("@/assets/img/cont01/contents_01_bg.jpg") no-repeat center / cover;
    overflow: hidden;
}

.contents__01__inner {
    max-width: 100%;
    padding-top: 130%; //height 값 조정
    position: relative;

    @media(max-width: 800px) {
        padding-top: 300%; 
    }

    .ct__img__01 {      
        @include common-img-style(25%, 20%, 14%, 20px);// $width, $left, $margin-top, $border-radius

        @media(max-width: 800px) {
            @include common-img-style(45%, 10%, 20%, 20px);
        }
    }

    .ct__img__02 {
        @include common-img-style(22%, 50%, 75%, 20px);

        @media(max-width: 800px) {
            @include common-img-style(50%, 45%, 126%, 20px);
        }
    }

    .ct__img__03 {
        @include common-img-style(16%, 36%, 24.5%, 15px);
        
        @media(max-width: 800px) {
            @include common-img-style(29%, 38.7%, 39.5%, 5px);
        }
    }

    .ct__img__04 {
        @include common-img-style(18%, 54%, 16%, 15px);

        @media(max-width: 800px) {
            @include common-img-style(35%, 71%, 23%, 15px);
        }
    }

    .ct__img__05 {
        @include common-img-style(11%, 76%, 35%, 15px);

        @media(max-width: 800px) {
            display: none;
        }
    }

    .ct__img__06 {
        @include common-img-style(10%, 90%, 25%, 15px);
        
        @media(max-width: 800px) {
            display: none;
        }
    }
    .ct__img__07 {
        @include common-img-style(27%, 5%, 70%, 0px);

        @media(max-width: 800px) {
            @include common-img-style(63%, -5%, 165%, 0px);
        }
    }


}
</style>