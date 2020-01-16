<template>
    <div>
        <text-block :data="textBlock1" />

        <div class="top-bot-paddimg">
            <v-container>
                <!-- <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                    <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">Складові
                        майстерності </span>
                    ХОРТИНГ ФЕХТУВАННЯ
                </h2> -->
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    ХОРТИНГ ФЕХТУВАННЯ - це сучасний український повноконтактний вид спорту, в основі якого покладено
                    мистецтво володіння шаблею, яка була історично розповсюджена на території сучасної України в період
                    між 16 та 17 віками н.э. А головною ціллю змагань є демонстрація бездоганної шабельної техніки й
                    майстерства шаблевого двобою в найкращих традиціях Запорізького козацтва.
                </p>

                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    ХОРТИНГ ФЕХТУВАННЯ, як сучасне мистецтво і як спорт, засноване на історичних бойових та оздоровчих
                    традиціях Запорізького козацтва. Задля того, щоб забезпечити найбільш повну відповідність
                    спортивного двобою до середньовічного бою, у ХОРТИНГ ФЕХТУВАННІ розроблені унікальні правила змагань
                    та впроваджено спеціальний рейтинг майстерності спортсменів-фехтувальників, що дозволяє об’єктивно
                    оцінювати їх рівень фехтування.
                </p>

                <a href="#">ССЫЛКА НА ПРАВИЛА</a>
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
                    subtitle_top: 'ПРАВИЛА',
                    title: 'ПРАВИЛА ЗМАГАНЬ',
                    boldText: 'ХОРТИНГ ФЕХТУВАННЯ - сучасний спорт з давньою традицією',
                    paragrafs: [
                        'Юні та дорослі хортинг фехтувальники будуть приймати участь у змаганнях, семінарах, атестаціях та показових виступах.',
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