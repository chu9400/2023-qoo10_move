<script setup>
    import {contData03} from "../constants/index.js";
</script>

<template>
    <section id="contents__03" class="contents__03__wrap">
        <div class="contents__03__inner">

            <div class="ct__img__03_00 cont03__ani">    
                <picture>
                    <source media="(max-width: 800px)" :srcset="contData03[7]">
                    <img :src="contData03[0]" alt="콘텐츠 이미지 00">
                </picture>
            </div>

            <div class="ct__img__03_01 cont03__ani">
                <figure>
                    <img :src="contData03[1]" alt="콘텐츠 이미지 01">
                    <figcaption>콘텐츠 이미지 01</figcaption>
                </figure>
            </div>

            <div class="ct__img__03_02 cont03__ani">
                <figure>
                    <img :src="contData03[2]" alt="콘텐츠 이미지 02">
                    <figcaption>콘텐츠 이미지 02</figcaption>
                </figure>
            </div>

            <div class="ct__img__03_03 cont03__ani">    
                <picture>
                    <source media="(max-width: 800px)" :srcset="contData03[8]">
                    <img :src="contData03[3]" alt="콘텐츠 이미지 03">
                </picture>
            </div>

            <div class="ct__img__03_04 cont03__ani">
                <figure>
                    <img :src="contData03[4]" alt="콘텐츠 이미지 04">
                    <figcaption>콘텐츠 이미지 04</figcaption>
                </figure>
            </div>

            <div class="ct__img__03_05 cont03__ani">
                <figure>
                    <img :src="contData03[5]" alt="콘텐츠 이미지 05">
                    <figcaption>콘텐츠 이미지 05</figcaption>
                </figure>
            </div>

            <div class="ct__img__03_06">
                <figure>
                    <img :src="contData03[6]" alt="콘텐츠 이미지 06">
                    <figcaption>콘텐츠 이미지 06</figcaption>
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
            this.animation03();
        },
        methods: {
            animation03() {

                const aniElements = document.querySelectorAll(".cont03__ani");

                    aniElements.forEach((element) => {

                    gsap.from(element, {
                        autoAlpha: 0,
                        y: 100,
                        scrollTrigger: {
                        trigger: element,
                        start: "top bottom",
                        end: `+=500`,
                        markers: false,
                        id: element,
                        scrub: 1,
                        },
                    });
                });

                // 무한반복 돌기
                gsap.to(".ct__img__03_06", {
                    rotate: 360, // 360도 회전
                    repeat: -1, // 무한 반복 
                    ease: "linear", // 일정한 속도로 회전
                    duration: 10, // 회전 속도
                });


                const growBigImg = document.querySelectorAll(".cont03__ani");
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

.contents__03__wrap {
    width: 100%;
    background: url("@/assets/img/cont03/contents_03_bg.jpg") no-repeat center / cover;
    overflow: hidden;
}

.contents__03__inner {
    width: 100%;
    position: relative;
    padding-top: 135%;

    @media(max-width: 800px) {
        padding-top: 370%;
    }
    
    .ct__img__03_00 {      
                            // $width, $left, $margin-top, $border-radius
        @include common-img-style(19%, 40%, 10%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include common-img-style(48%, 25%, 39%, 20px);
            z-index: 1;
        }
    }
    .ct__img__03_01 {      
        @include common-img-style(15%, 12%, 18%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include common-img-style(30%, 62%, 15%, 20px);
            
            figure {
                transform: scaleX(-1);
            }
        }
    }

    .ct__img__03_02 {      
        @include common-img-style(18%, 64%, 29%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include common-img-style(48%, 5%, 150%, 20px);
            z-index: 2;
        }
    }

    .ct__img__03_03 {      
        @include common-img-style(18%, 17%, 60%, 20px);
        position: absolute;
        top: 0;
        z-index: 1;

        @media(max-width: 800px) {
            @include common-img-style(50%, 43%, 205%, 20px);
        }
    }

    .ct__img__03_04 {      
        @include common-img-style(13%, 73%, 79%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            display: none;
        }
    }

    .ct__img__03_05 {      
        @include common-img-style(25%, 53%, 90%, 20px);
        position: absolute;
        top: 0;
        z-index: 1;

        @media(max-width: 800px) {
            @include common-img-style(40%, 13%, 294%, 20px);
            z-index: 0;
        }
    }

    .ct__img__03_06 {      
        @include common-img-style(25%, 22%, 90%, 20px);
        position: absolute;
        top: 0;
        z-index: 0;

        @media(max-width: 800px) {
            @include common-img-style(62%, 67%, 155%, 20px);

        }
    }


}
</style>