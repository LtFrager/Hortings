<template>
    <div>
        <my-map />

        <h2 data-aos="zoom-in" data-aos-duration="1000" data-aos-delay="300"
            class="std__title text__black text-xs-center">
            <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">контакти </span>
            Секцiй
        </h2>

        <v-container>
            <v-layout row wrap>
                <v-flex xs12 sm6 md4 v-for="item in 16" :key="item">
                    <h3>City</h3>
                    <ul>
                        <li>
                            section name
                        </li>

                        <li>
                            section name
                        </li>

                        <li>
                            section name
                        </li>

                        <li>
                            section name
                        </li>
                    </ul>
                </v-flex>
            </v-layout>
        </v-container>
    </div>

</template>
<script>
    import PromoCards from '@/components/PromoCards'
    import TitlePromo from '@/components/TitlePromo'
    import ListBlock from '@/components/ListBlock'
    import TextBlock from '@/components/TextBlock'
    import MyMap from '@/components/MyMap'
    export default {
        components: {
            PromoCards,
            TitlePromo,
            ListBlock,
            TextBlock,
            MyMap
        },
        data() {
            return {
                textBlock: [{
                    textLeft: true,
                    img: '/img/index/index3.jpg',
                    subtitle_top: 'Gladiatoria',
                    title: 'ГДЕ ПРОХОДЯТ ЗАНЯТИЯ?',
                    boldText: ' Club Gladiatoria - это инициативная группа энтузиастов-исследователей и любителей искусства фехтования клинковым оружием. ',
                    paragrafs: [
                        ' С 1-го сентября - в зале № 229 спортивного комплекса Киевского университета имени Бориса Гринченко по адресу ул.Маршала Тимошенко 13Б, ст. метро Минская.',
                        'В теплое время - на открытой площадке возле ст. метро Оболонь рядом со школой-лицеем №157.',
                    ]
                }],


                titlePromoGoToTraining: [{
                    img: '/img/about/image2.jpg ',
                    subtitle_top: 'ЗАПИСАТЬСЯ НА ТРЕНИРОВКУ',
                    title: 'Первая тренеровка бесплатно',
                    subtitle_bottom: 'Наши телефоны: 068 978-48-85, 095 282-09-67, 073 155-39-07,E-mail: horting.fencing@gmail.com, kendo.obolon@gmail.com ',
                }],

            }
        }
    }
</script>
<style lang="scss" scoped>

</style>