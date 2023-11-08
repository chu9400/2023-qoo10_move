<script setup>
    import {contData02} from "../constants/index.js";
</script>

<template>
    <section id="contents__03" class="contents__03__wrap">
        

    
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

               console.log("animation03");
            }
        }
    }
    
</script>

<style lang="scss">

@import "../assets/scss/vars.scss";

.contents__03__wrap {
    width: 100%;
    height: 500px;
    //background: url("@/assets/img/contents_02_bg.jpg") no-repeat center / cover;
    background-color: #333;
    overflow: hidden;
}


</style>