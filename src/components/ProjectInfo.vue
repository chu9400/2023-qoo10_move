<template>
    <section id="ProjectInfo" class="pi__wrap">

        <div class="pi__inner">
            <div class="pi_left">
                <h2 class="pi__title">새로운 패션 플랫폼 큐텐 무브</h2>
                <p class="pi__desc">
                    비디오 기반의 플랫폼을 구축하고 큐레이션을 통해 브랜드 경험을 제공함으로써 상품 구매와도 연계되는 선순환 구조를 이룹니다. <br />
                    적극적으로 상품을 보여주고, 추천하고, 찾아주고, 비교해 주는 큐레이션을 통해 콘텐츠와 커머스의 경계를 허물고<br />
                    불특정 다수에게 일방적인 서비스를 제공하는 것이 아닌 다양한 콘텐츠를 개인화된 서비스로 제공합니다.<br />
                    다크모드를 제공함으로써 개인의 사용자가 다양한 환경에서 서비스를 원활하게 이용할 수 있도록 하였습니다.<br />
                </p>
            </div>

            <div class="pi_right">
                <dl>
                    <dt>client</dt>
                    <dd>qoo10</dd>
                </dl>
                <dl>
                    <dt>division</dt>
                    <dd>ux consulting / design</dd>
                </dl>
                <dl>
                    <dt>launch</dt>
                    <dd>2022.04</dd>
                </dl>
                <dl>
                    <dt>url</dt>
                    <dd>
                        <a href="https://www.qoo10.jp/" target="_blank" rel="noopener" title="open in new tab" >www.qoo10.jp</a>
                    </dd>
                </dl>
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
            this.animation00();
        },
        methods: {
            animation00() {

                gsap.from(".pi__inner", { 
                    y : 50,
                    autoAlpha:0,
                    scrollTrigger: {
                    trigger: ".pi_left",
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

.pi__wrap {
    background-color: #fff;
    width: 100%;
    height: auto;
    box-sizing: border-box;
    margin: 0 auto;
}


.pi__inner {
    padding: 150px 50px;
    margin: 0 auto;
    max-width: 1440px;
    box-sizing: border-box;    
    display: flex;
    justify-content: space-between;

    @media(max-width: 1200px) {
        padding: 120px 50px;
        flex-direction: column;
    }

    .pi_left {
        min-width: 780px;
        font-size: 18px;
        letter-spacing: -.05em;

        @media(max-width: 1200px) {
            min-width: 100%;
            margin-bottom: 5vh;
        }

        @media(max-width: 480px) {
            font-size: 14px;
        }

        .pi__title {
            margin-bottom: 2vh;
            font-weight: 900;
            transform : rotate(0.04deg); 
        }

        .pi__desc {
            width: 100%;
            font-size: 14px;
            font-weight: 500;
            letter-spacing: -.05em;
            line-height: 26px;
            transform : rotate(0.04deg); 
            word-break: keep-all;

            @media(max-width: 480px) {
                font-size: 13px;
            }
        }
    }

    .pi_right {
        width: 400px;
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;

        @media(max-width: 1200px) {
            width: 100%;
        }

        dl {
            width: 50%;
            margin-bottom: 4vh;
            transform : rotate(0.04deg); 

            @media(max-width: 1200px) {
                margin-bottom: 1vh;
            }

            dt {
                margin-bottom: 1vh;
                font-weight: 700;
                
            }
        }
    }

}
</style>