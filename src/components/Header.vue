<script setup>
import {logoImg} from "../constants/index.js";
</script>

<template>
    <header id="header">
        <div class="nullDiv"></div>
        <div class="video__inner">
            <video muted loop autoplay> <!-- autoplay -->
                <source src="https://www.cttd.co.kr/_nuxt/qoo10_move_pc.6465939e.mp4" type="video/mp4" width>
            </video>

            <div class="logo__inner">
                <figure class="growBig">
                    <img :src="logoImg" alt="로고">
                </figure>
                <p class="growBig">app & web ux design</p>
            </div>
        </div>
    </header>
    
</template>

<style lang="scss">
    .nullDiv {
        width: 100%;
        height: 100vh;
    }

    .video__inner {
        width: 100%;
        height: 100vh;
        position: fixed;
        top: 0;
        overflow: hidden;
        background-color: #333;

        video {
            width: 100%;
            height: 100%;
            object-fit: cover; // 영상을 화면에 가득차게
        }
    }

    .logo__inner {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);

        figure {
            width: clamp(210px, 144px + 18.3vw, 408px);
        }
        
        p {
            margin-top: 50px;
            color: #fff;
            font-size: clamp(15px, 12px + 0.83vw, 24px);
            font-weight: 700;
            line-height: 1;
            text-align: center;

            @media (max-width:480px) {
                margin-top: 20px;
            }
        }
    }
</style>