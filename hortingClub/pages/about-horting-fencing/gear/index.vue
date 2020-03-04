<template>
    <div>
        <text-block :data="textBlockAboutUs" />

        <div class="top-bot-paddimg">
            <v-container>
                <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                    <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                        class="subtitle">Спорядження</span>
                    Спорядження для початкового та для основного рівня занять
                </h2>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    Для початкових занять з ХОРТИНГ ФЕХТУВАННЯ дітям та їх батькам потрібно мати:<br>
                    - спортивну форму (штани та футболку, або, якщо вже є, форму для хортинг фехтування);<br>
                    - змінне взуття для залу (кросівки або фехтувальні специ);<br>
                    - питну воду;<br>
                    - стандартну медичну довідку, що дозволяє заняття фізкультурою та спортом.<br>
                </p>
            
                <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                    <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle"></span>
                    "Синтшабля"
                </h2>
                <img width="100%" src="/img/gear/SynthSaber0.jpg" alt="">
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    1) вістря клинка;<br>
                    2) лезо клинка;<br>
                    3) обух клинка;<br>
                    4) гарда;<br>
                    5) дужка гарди;<br>
                    6) рукоятка;<br>
                    7) яблуко рукоятки.
                </p>

                  <div style="text-align:center">
                    <img style="max-width:640px;" width="100%" src="/img/gear/hf_uniform_set.jpg" alt="">

                     <img style="max-width:640px;" width="100%" src="/img/gear/junior_hf_gear.jpg" alt="">

                      <img style="max-width:640px;" width="100%" src="/img/gear/senior-adult_hf_gear.jpg" alt="">
                </div>

                <a href="/downloads/horting fencing equipment for training.doc" download>Скачать список снаряжения</a>
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
                    img: '/img/about-horting/gear0.jpg',
                    subtitle_top: 'СПОРЯДЖЕННЯ ТА ЕКІПІРУВАННЯ',
                    title: 'Битися так, як билися наші предки!',
                    boldText: 'Практика ХОРТИНГ ФЕХТУВАННЯ передбачає використання спеціальних обладунків та синтетичних клинків «синтшабель»',
                    paragrafs: [
                        'які зводять до мінімуму ризик травмування, але зберігають можливість рухатись вільно та швидко, наносити удари шаблею в усю міць, дозволяють у повній мірі проявити себе, свою сміливість, силу й характер у фехтувальному двобої так, як це робили наші предки.',
                    ]
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