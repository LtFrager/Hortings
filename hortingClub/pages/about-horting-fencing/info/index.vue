<template>
    <div>
        <text-block :data="textBlock1" />

        <div class="top-bot-paddimg">
            <v-container>
                <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                    <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">ХОРТИНГ
                        ФЕХТУВАННЯ </span>
                    більш ніж спорт!
                </h2>

                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    В основі ХОРТИНГ ФЕХТУВАННЯ покладена науково організована система навчання, всебічного розвитку,
                    морально-етичного виховання й оздоровлення дорослих, дітей та молоді.
                </p>

                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    Мистецтво ХОРТИНГ ФЕХТУВАННЯ складається з таких взаємопов’язаних між собою напрямів: <br>
                    1. Історико-філософський.<br>
                    2. Навчально-виховний.<br>
                    3. Фізкультурно-оздоровчий.<br>
                    4. Спортивно-прикладний.<br>
                    5. Військово-патріотичний.<br>
                </p>


                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    ХОРТИНГ ФЕХТУВАННЯ - це шлях впродовж життя,
                    їм можуть займатися як дорослі, так і діти, чоловіки та жінки без жодних вікових,
                    вагових та інших обмежень! Практика ХОРТИНГ ФЕХТУВАННЯ формує дисципліну, характер, дух та волю,
                    системність та критичність мислення, зміцнює витривалість та увагу, корегує осанку, ходу, грацію й
                    координацію рухів.
                </p>
            </v-container>
        </div>

        <!-- <v-parallax style="height:auto" src="/img/about-horting/2.jpg">
            <v-container>
                <v-layout row justify-end align-center fill-height>
                    <v-flex xs12 sm8 md7>
                        <list-block :data="ListBlockData" :titleData="ListBlockTitle" />
                    </v-flex>
                </v-layout>
            </v-container>
        </v-parallax> -->

        <!-- <title-promo :data="titlePromoData" /> -->

        <text-block :data="textBlock2" />

        <div class="top-bot-paddimg">
            <v-container>
                <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                    <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle"></span>
                    Також НФХФУ активно розробляє тренувальні програми для людей з обмеженнями опорно-рухового апарату.
                </h2>

                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    Практика ХОРТИНГ ФЕХТУВАННЯ дозволяє: <br>
                    покращити моторику та координацію рухів;
                    оптимізувати узгодженість роботи опорно-рухового апарату з корою головного мозку; <br>
                    знімати хронічне м’язове перенапруження, стрес; <br>
                    попереджувати деградацію м’язових тканин та суглобів; <br>
                    розвинути витривалість та зміцнити серцево-судинну систему; <br>
                    компенсувати функціональні обмеження; <br>
                    створити індивідуальний стиль фехтування з урахуванням фізіологічних особливостей; <br>
                    брати участь у двобоях та турнірах разом з усіми! <br>
                </p>

            </v-container>
        </div>
    </div>
</template>
<script>
    import TitlePromo from '@/components/TitlePromo'
    import ListBlock from '@/components/ListBlock'
    import TextBlock from '@/components/TextBlock'
    export default {
        components: {
            TitlePromo,
            ListBlock,
            TextBlock
        },
        data() {
            return {
                textBlock1: [{
                    textLeft: true,
                    img: '/img/about-horting/1.jpg',
                    subtitle_top: 'ЗАГАЛЬНА ІНФОРМАЦІЯ',
                    title: 'ХОРТИНГ ФЕХТУВАННЯ?',
                    boldText: 'ХОРТИНГ ФЕХТУВАННЯ, або український шаблевий двобій',
                    paragrafs: [
                        'новітній український вид спорту, бойове мистецтво та засіб оздоровлення тіла і духу, що сьогодні активно розвивається в Україні! Він поєднує в собі фехтування на шаблях з елементами рукопашної боротьби ХОРТИНГ.',
                    ]
                }],

                titlePromoData: [{
                    img: '/img/about-horting/3.jpg',
                    subtitle_top: 'ХОРТИНГ ФЕХТУВАННЯ',
                    title: 'фехтування для всіх!',
                    subtitle_bottom: 'ХОРТИНГ ФЕХТУВАННЯ - це інклюзивний вид спорту, займатись яким можна починаючи вже з 6 років. В ньому немає ніяких вікових та гендерних обмежень!'
                }],

                textBlock2: [{
                    textLeft: false,
                    img: '/img/about-horting/1.jpg',
                    subtitle_top: 'ХОРТИНГ ФЕХТУВАННЯ',
                    title: 'фехтування для всіх!',
                    boldText: 'ХОРТИНГ ФЕХТУВАННЯ - це інклюзивний вид спорту, займатись яким можна починаючи вже з 6 років. В ньому немає ніяких вікових та гендерних обмежень!',
                    paragrafs: []
                }],
            }
        }
    }
</script>

<style lang="scss" scoped>
    .top-bot-paddimg {
        padding: 100px 0px;
    }

    .temp-list {
        padding: 0px;
        list-style-type: none;

        li {
            display: flex;
            margin-bottom: 36px;

        }
    }
</style>