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
    background-color: #333;
    width: 100%;
    height: 500px;
    box-sizing: border-box;
}


.pi__inner {
    padding: 150px 50px;
    margin: 0 auto;
    max-width: 1440px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .pi__header {
        width: 70%;
    }

    .pi__data {
        width: 30%;
        display: flex;
        flex-wrap: wrap;        

        .pi__data__list {
            background-color: #fff;
            width: 50%;
            /* 여기에 플레스줄까? */
            

            dl {
                
            }
        }

        

    }
}
</style>