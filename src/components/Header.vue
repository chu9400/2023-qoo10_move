<template>
    <header id="header">
        <div class="nullDiv"></div>
        <div class="video__inner">
            <video muted loop autoplay> <!-- autoplay -->
                <source src="https://www.cttd.co.kr/_nuxt/qoo10_move_pc.6465939e.mp4" type="video/mp4" width>
            </video>
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
</style>