<script setup>
    import {contData04} from "../constants/index.js";
</script>

<template>
    <section id="contents__04" class="contents__04__wrap">
        <div class="contents__04__inner">

            <div class="ct__img__04_00">    
                <picture>
                    <!-- <source media="(max-width: 800px)" :srcset="contData04[7]"> -->
                    <img :src="contData04[0]" alt="콘텐츠 이미지 00">
                </picture>
            </div>
            <div class="ct__img__04_01">    
                <picture>
                    <img :src="contData04[1]" alt="콘텐츠 이미지 01">
                </picture>
            </div>

            <div class="ct__img__04_02">    
                <picture>
                    <img :src="contData04[2]" alt="콘텐츠 이미지 02">
                </picture>
            </div>

            <div class="ct__img__04_03">    
                <picture>
                    <img :src="contData04[3]" alt="콘텐츠 이미지 03">
                </picture>
            </div>

            <div class="ct__img__04_04">    
                <picture>
                    <img :src="contData04[4]" alt="하트 이미지">
                </picture>
            </div>

            <div class="ct__img__04_05">    
                <picture>
                    <img :src="contData04[5]" alt="좋아요 이미지00">
                </picture>
            </div>

            <div class="ct__img__04_06">    
                <picture>
                    <img :src="contData04[6]" alt="좋아요 이미지01">
                </picture>
            </div>

            <div class="ct__img__04_07">    
                <picture>
                    <img :src="contData04[7]" alt="좋아요 이미지02">
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
            this.animation04();
        },
        methods: {
            animation04() {

                gsap.fromTo(".ct__img__04_00", 
                    { scale: 0.5, rotate: -10, },
                    { scale: 1, rotate: 0, 
                        scrollTrigger: {
                            trigger: ".ct__img__04_00",
                            start: "top bottom",
                            end: `+=500`,
                            scrub: 1,
                        },
                    }
                );

                gsap.fromTo(".ct__img__04_01", 
                    { scale: 0.5, rotate: 0, },
                    { scale: 1, rotate:15, 
                        scrollTrigger: {
                            trigger: ".ct__img__04_00",
                            start: "top bottom",
                            end: `+=500`,
                            scrub: 1,
                        },
                    }
                );

                gsap.fromTo(".ct__img__04_02", 
                    { scale: 0.5, rotate: 0, },
                    { scale: 1, rotate:10, 
                        scrollTrigger: {
                            trigger: ".ct__img__04_02",
                            start: "top bottom",
                            end: `+=500`,
                            scrub: 1,
                        },
                    }
                );

                gsap.fromTo(".ct__img__04_03", 
                    { scale: 0.5, rotate: 0, },
                    { scale: 1, rotate:-8, 
                        scrollTrigger: {
                            trigger: ".ct__img__04_03",
                            start: "top bottom",
                            end: `+=500`,
                            scrub: 1,
                        },
                    }
                );



                // 좋아요 애니메이션
                const likeAni01 = gsap.timeline();
                likeAni01.from(".ct__img__04_05", {y: -50, autoAlpha:0, })
                    .to(".ct__img__04_05", {y: -0, autoAlpha:1, })
                    .to(".ct__img__04_05", {y: -30, duration:2, ease:'none', yoyo:true, repeat:-1,})
                    
                ScrollTrigger.create({
                    animation: likeAni01,
                    trigger: ".ct__img__04_05",
                    start: "top bottom",
                });

                const likeAni02 = gsap.timeline();
                likeAni02.from(".ct__img__04_06", {y: -50, autoAlpha:0,})
                    .to(".ct__img__04_06", {y: -0, autoAlpha:1,})
                    .to(".ct__img__04_06", {y: -20, duration:2, ease:'none', yoyo:true, repeat:-1, delay:1})
                    
                ScrollTrigger.create({
                    animation: likeAni02,
                    trigger: ".ct__img__04_06",
                    start: "top bottom",
                    
                });

                const likeAni03 = gsap.timeline();
                likeAni03.from(".ct__img__04_07", {y: -50, autoAlpha:0,})
                    .to(".ct__img__04_07", {y: -0, autoAlpha:1,})
                    .to(".ct__img__04_07", {y: -20, duration:2, ease:'none', yoyo:true, repeat:-1,})
                    
                ScrollTrigger.create({
                    animation: likeAni03,
                    trigger: ".ct__img__04_07",
                    start: "top bottom",
                    
                });
                // 좋아요 애니메이션 end
               
            }
        }
    }
    
</script>

<style lang="scss">

@import "../assets/scss/vars.scss";

.contents__04__wrap {
    width: 100%;
    background: url("@/assets/img/cont04/contents_04_bg.jpg") no-repeat center / cover;
    overflow: hidden;
}

.contents__04__inner {
    width: 100%;
    position: relative;
    padding-top: 100%;

    @media(max-width: 800px) {
        padding-top: 255%;
    }
    
    .ct__img__04_00 {      
                            // $width, $left, $margin-top, $border-radius
        @include cont01-img-style(23%, 23%, 10%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(47%, 25%, 28%, 20px);
        }
    }

    .ct__img__04_01 {      
        @include cont01-img-style(17%, 30%, 21%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(35%, 40%, 50%, 20px);
        }
    }

    .ct__img__04_02 {      
        @include cont01-img-style(18%, 61%, 37%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(40%, 45%, 128%, 20px);
        }
    }

    .ct__img__04_03 {      
        @include cont01-img-style(18%, 46.5%, 58.5%, 20px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(40%, 14%, 153%, 20px);
        }
    }

    .ct__img__04_04 {      
        @include cont01-img-style(5%, 19%, 33%, 0px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(12%, 16%, 77%, 0px);
        }
    }

    .ct__img__04_05 {      
        @include cont01-img-style(17%, 77%, 6%, 0px);
        position: absolute;
        top: 0;

        @media(max-width: 800px) {
            @include cont01-img-style(25%, 66%, -1%, 0px);
        }
    }

    .ct__img__04_06 {      
        @include cont01-img-style(10%, 0%, 65%, 0px);
        position: absolute;
        top: 0;
        @media(max-width: 800px) {
            @include cont01-img-style(18%, 0%, 119%, 0px);
        }
    }

    .ct__img__04_07 {      
        @include cont01-img-style(26%, 10%, 77%, 20px);
        position: absolute;
        top: 0;
        @media(max-width: 800px) {
            @include cont01-img-style(40%, 70%, 215%, 20px);
        }
    }




}
</style>