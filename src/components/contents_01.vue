<script setup>
    import {contData01} from "../constants/index.js";
    
</script>

<template>
    <section id="contents__01" class="contents__01__wrap">
        <div class="contents__01__inner">
            <div class="ct__img__01">
                <figure>
                    <img :src="contData01[0]" alt="콘텐츠 이미지 01">
                    <figcaption>콘텐츠 이미지 01</figcaption>
                </figure>
            </div>

            <div class="ct__img__02">
                <figure>
                    <img :src="contData01[1]" alt="콘텐츠 이미지 02">
                    <figcaption>콘텐츠 이미지 02</figcaption>
                </figure>
            </div>

            <div class="ct__img__03">
                <figure>
                    <img :src="contData01[2]" alt="콘텐츠 이미지 03">
                    <figcaption>콘텐츠 이미지 03</figcaption>
                </figure>
            </div>

            <div class="ct__img__04">
                <figure>
                    <img :src="contData01[3]" alt="콘텐츠 이미지 04">
                    <figcaption>콘텐츠 이미지 04</figcaption>
                </figure>
            </div>

            <div class="ct__img__05">
                <figure>
                    <img :src="contData01[4]" alt="콘텐츠 이미지 05">
                    <figcaption>콘텐츠 이미지 05</figcaption>
                </figure>
            </div>

            <div class="ct__img__06">
                <figure>
                    <img :src="contData01[5]" alt="콘텐츠 이미지 06">
                    <figcaption>콘텐츠 이미지 06</figcaption>
                </figure>
            </div>
            <div class="ct__img__07">
                <figure>
                    <img :src="contData01[6]" alt="콘텐츠 이미지 07">
                    <figcaption>콘텐츠 이미지 07</figcaption>
                </figure>
            </div>

        </div>
    </section>
</template>

<style lang="scss">

@import "../assets/scss/vars.scss";

.contents__01__wrap {
    width: 100%;
    height: 2200px;
    background: url("@/assets/img/contents_01_bg.jpg") no-repeat center / cover;
    overflow: hidden;
}

.contents__01__inner {
    max-width: 100%;
    position: relative;

    /* 각 이미지마다 반응형 일때 max-wdith 값 조정 */

    .ct__img__01 {      
        @include cont01-img-style(25%, 20%, 14%, 20px);// $width, $left, $margin-top
    }

    .ct__img__02 {
        @include cont01-img-style(25%, 52%, 70%, 20px);
    }

    .ct__img__03 {
        @include cont01-img-style(16%, 36%, 24.5%, 15px);
    }

    .ct__img__04 {
        @include cont01-img-style(18%, 54%, 16%, 15px);
    }

    .ct__img__05 {
        @include cont01-img-style(11%, 76%, 30%, 15px);

        @media(max-width: 800px) {
            display: none;
        }
    }

    .ct__img__06 {
        @include cont01-img-style(10%, 90%, 21%, 15px);
        
        @media(max-width: 800px) {
            display: none;
        }
    }
    .ct__img__07 {
        @include cont01-img-style(27%, 0%, 63%, 0px);
    }

    
}
</style>