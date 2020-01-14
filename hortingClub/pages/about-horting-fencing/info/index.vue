<template>
    <div>
        <text-block :data="textBlockAboutUs" />

        <div class="top-bot-paddimg">
            <v-container>
                <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                    <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">Які задачи
                        вирішуватиме </span>
                   info
                </h2>

                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    иховання зростаючого покоління у дусі патріотизму, поваги до української національної історії і
                    традицій, лідерства і дисциплінованості, товариства, взаємодопомоги, та відповідальності за долю
                    держави;
                </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    підвищення престижу Української держави; </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    розвиток фізичних здібностей, вольових, ментально-психологічних і морально-етичних якостей у
                    громадян;
                </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    формування у громадян навичок критичного мислення та здорового способу життя;
                </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    разом з іншими дисциплінами хортингу, будуватиме єдину систему національних спортивних та бойових
                    мистецтв України, яка сформує каркас освітньо-оздоровчого комплексу української нації, та стане
                    гарантом
                    її безпеки, добробуту й майбутнього.
                </p>
            </v-container>
        </div>

        <v-parallax style="height:auto" src="/img/about-horting/2.jpg">
            <v-container>
                <v-layout row justify-end align-center fill-height>
                    <v-flex xs12 sm8 md7>
                        <list-block :data="ListBlockData" :titleData="ListBlockTitle" />
                    </v-flex>
                </v-layout>
            </v-container>
        </v-parallax>

        <div class="top-bot-paddimg">
            <v-container>
                <v-layout class="padding" row align-center fill-height>
                    <v-flex xs12 sm8 md6>
                        <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                            <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                                class="subtitle">Стратегічні
                                напрями</span>
                            ХОРТИНГ ФЕХТУВАННЯ
                        </h2>
                        <p data-aos="fade-up" data-aos-duration="1000" class="text__black std__text"> В основі хортинг
                            фехтування</p>
                        <p data-aos="zoom-in-up" data-aos-duration="1200" class="std__text">
                            багаторічна науково організована система навчання, всебічного розвитку,
                            морально-етичного виховання й оздоровлення.
                        </p>
                    </v-flex>
                    <v-flex xs12 sm12 md6>
                        Нужна картинка
                        <ul class="temp-list">
                            <li>
                                1. Історико-філософський
                            </li>
                            <li>
                                2. Навчально-
                                виховний

                            </li>
                            <li>
                                3. Фізкультурно-
                                оздоровчий

                            </li>
                            <li>
                                4. Спортивно-
                                професійний

                            </li>
                            <li>
                                5. Військово-
                                патріотичний

                            </li>
                        </ul>
                    </v-flex>
                </v-layout>
            </v-container>
        </div>

        <title-promo :data="titlePromoData" />

        <div class="top-bot-paddimg">
            <v-container>
                <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                    <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">Складові
                        майстерності </span>
                    ХОРТИНГ ФЕХТУВАННЯ
                </h2>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    1. «Кондиціями» визначається те, що учень потенційно спроможній зробити. </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    2. «Моторні навички» - це вміння виконувати ті чи інші рухи самі по собі, у відриві від контексту.
                </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    3. «Технічні навички» - вміння вирішувати з допомогою тих чи інших рухів та дій конкретні задачі,
                    вміння
                    застосовувати рухи у бойовій ситуації з урахуванням дій супротивника.</p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    4. «Тактичні навички» - аналіз дій супротивника, прогноз його рухів та його реакції на ті чи інші
                    дії
                    спортсмена-фехтувальника. Тактика починається там, де на місце безпосередньої реакції на дії
                    супротивника приходить робота з інформацією, усвідомлене планування особистих дій та використання
                    або
                    руйнування планів супротивника. </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    5. «Стратегія» - це постановка задач та визначення пріоритетів на тренування, змагання або на
                    конкретний
                    двобій з урахуванням зовнішніх факторів.</p>
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
                textBlockAboutUs: [{
                    textLeft: true,
                    img: '/img/about-horting/1.jpg',
                    subtitle_top: 'Що таке',
                    title: 'ХОРТИНГ ФЕХТУВАННЯ ?',
                    boldText: 'Хортинг фехтування – в перспективі національний вид спорту України.',
                    paragrafs: [
                        ' Він поєднує в собі мистецтво фехтування на  шаблях, що були на озброєнні козаків у 16-17 сторіччях та рукопашну боротьбу хортинг.',
                    ]
                }],
                ListBlockTitle: [{
                    subtitle: '3авдяки чому?',
                    title: '3авдяки чому?'
                }],
                ListBlockData: [{
                        icon: '1',
                        title: 'Безпека',
                        text: ' Передові сучасні технологічні рішення, використані у розробці спортивного та тренувального обладнання.',
                    },
                    {
                        icon: '2',
                        title: 'Наука',
                        text: 'Науково обгрунтована комплексна система навчання, виховання та тренування учнів.',
                    },
                    {
                        icon: '3',
                        title: 'Правила',
                        text: 'Унікальні правила змагань та система рейтингу майстерності фехтувальників. ',
                    },
                ],

                titlePromoData: [{
                    img: '/img/about-horting/3.jpg',
                    subtitle_top: 'Більш ніж спорт !',
                    title: 'ХОРТИНГ ФЕХТУВАННЯ',
                    subtitle_bottom: 'Це засіб виховання високоморальної, критично мислячої, вольової та цілеспрямованої людини, та засіб її успішної соціальної адаптації у сучасному високошвидкісному глобалізованому суспільстві. '
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