<template>
    <section id="ProjectInfo" class="pi__wrap">

        <div class="pi__inner">
            <div class="pi__header">
                <h2 class="pi__title">새로운 패션 플랫폼 큐텐 무브</h2>
                <p class="pi__desc">
                    비디오 기반의 플랫폼을 구축하고 큐레이션을 통해 브랜드 경험을 제공함으로써 상품 구매와도 연계되는 선순환 구조를 이룹니다. <br />
                    적극적으로 상품을 보여주고, 추천하고, 찾아주고, 비교해 주는 큐레이션을 통해 콘텐츠와 커머스의 경계를 허물고<br />
                    불특정 다수에게 일방적인 서비스를 제공하는 것이 아닌 다양한 콘텐츠를 개인화된 서비스로 제공합니다.<br />
                    다크모드를 제공함으로써 개인의 사용자가 다양한 환경에서 서비스를 원활하게 이용할 수 있도록 하였습니다.<br />
                </p>
            </div>

            <div class="pi__data">
                <div class="pi__data__list">
                    <dl>
                        <dt>clien</dt>
                        <dd>qoo10</dd>
                    </dl>
                </div>
                <div class="pi__data__list">
                    <dl>
                        <dt>division</dt>
                        <dd>ux consulting / design</dd>
                    </dl>
                </div>
                <div class="pi__data__list">
                    <dl>
                        <dt>launch</dt>
                        <dd>2022.04</dd>
                    </dl>
                </div>
                <div class="pi__data__list">
                    <dl>
                        <dt>url</dt>
                        <dd>
                            <a href="www.qoo10.jp" target="_blank" rel="noreferrer noopener">www.qoo10.jp</a>
                        </dd>
                    </dl>
                </div>
            </div>

        </div>
        
    </section>
</template>

<style lang="scss">

.pi__wrap {
    background-color: #fff;
    width: 100%;
    height: auto;
    box-sizing: border-box;
}


.pi__inner {
    padding: 150px 50px;
    margin: 0 auto;
    max-width: 1440px;
    display: flex;
    justify-content: space-between;
    box-sizing: border-box;

    @media(max-width:1080px){
        flex-direction: column
    }

    .pi__header {
        width: 60%;
        max-width: 780px;

        @media(max-width:1080px){
            width: 100%;
        }

        .pi__title {
            font-size: 2rem;
            margin: 25px 0;
            font-weight: 700;
        }

        .pi__desc {
            font-size: 0.9rem;
            line-height: 1.8;

            @media(max-width:1080px){
                margin-bottom: 10vh;
            }
        }
    }

    .pi__data {
        width: 40%;
        max-width: 450px;
        display: flex;
        align-items: flex-end;
        flex-wrap: wrap; 
        
        @media(max-width:1080px){
            width: 100%;
            max-width: 100%;
        }

        .pi__data__list {
            background-color: #fff;
            width: 50%;
            

            dl {
                width: 100%;
             
                @media(max-width:1080px){
                    margin-bottom: 1vh;
                }

                dt {
                    margin-bottom: 1vh;
                    font-weight: 700;
                }
            }
        }
    }
}
</style>