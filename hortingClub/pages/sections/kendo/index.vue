<template>
    <div>
        <text-block :data="textBlockKendo" />

        <v-parallax style="height:auto" src="/img/about/image4.jpg">
            <v-container>
                <v-layout row justify-end align-center fill-height>
                    <v-flex xs12 sm7 md6>
                        <list-block :data="ListBlockData" :titleData="ListBlockTitle" />
                    </v-flex>
                </v-layout>
            </v-container>
        </v-parallax>

        <title-promo :data="titlePromoData_2" />

        <v-container>
            <div>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    О сновным принципом Кэндо является единство духа (Ки), меча (Кэн) и тела (Тай), что в современной
                    трактовке соответствует эмоциям и чувствам, интеллекту (меч как символ разума) и телесному здоровью
                    (в том числе моторике, координации и сенсорике). То есть в процессе тренировок происходит
                    гармоничное развитие как ф изических, так и психологических аспектов личности. П реодолевая
                    кажущ ееся неразреш имым противоречие между духовным и материальным началами современного
                    человека, Кэндо соединяет их в единую систему, позволяя наилучш им образом раскрыть и реализовать
                    заложенный в человеке потенциал.
                </p>
                <img style="max-width:50%;float:left;margin:12px" src="/img/about/trainers/team-1.jpg" alt="img"
                    data-aos="fade-right" data-aos-duration="1000">
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    Кэндо подходит как мужчинам, так и женщ инам всех возрастов. А также детям.
                </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    Кэндо полезно всем, но особенно тем, у кого:</p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    - есть трудности с самовыражением и с дисциплиной;</p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    - проблемы с самооценкой и уверенностью в себе;</p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    - есть потребность в ф изическом развитии и в коррекции осанки;</p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    - хроническое перенапряжение - стресс;</p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    - дисбаланс между духовной и интеллектуальной сф ерами жизни;</p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    - творческий и духовный кризис, повыш енная тревожность и раздражительность;</p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    - стоит вопрос, куда отдать ребенка, чтобы укрепить его духовно и ф изически?
                </p>

            </div>

        </v-container>

        <title-promo :data="titlePromoGoToTraining" />

    </div>
</template>
<script>
    import PromoCards from '@/components/PromoCards'
    import TitlePromo from '@/components/TitlePromo'
    import ListBlock from '@/components/ListBlock'
    import TextBlock from '@/components/TextBlock'
    export default {
        components: {
            PromoCards,
            TitlePromo,
            ListBlock,
            TextBlock
        },
        data() {
            return {
                textBlockKendo: [{
                    textLeft: true,
                    img: '/img/horting/hort2.jpg',
                    subtitle_top: 'Gladiatoria',
                    title: 'Кэндо',
                    boldText: 'Кэндо, это соревновательное японское искусство фехтования.',
                    paragrafs: [
                        'Кэндо сочетает в себе спорт, многовековую культуру и историю, а самое главное - мощную, выработанную веками, психолого-педагогическую систему, направленную на развитие силы воли, боевого духа, на укрепление характера, здоровья и на воспитание гармоничной, высоконравственной личности.',
                    ]
                }],

                titlePromoData_1: [{
                    img: '/img/about/image2.jpg ',
                    title: 'Большой текст',
                    subtitle_bottom: 'Малый текст, можно добавить кнопку'
                }],

                titlePromoData_2: [{
                    img: '/img/kendo/kendo4.jpg',
                    subtitle_top: 'Первый дан за полгода',
                    title: 'Программа подготовки кэндоистов Секции Кэндо клуба “GLADIATORIA”',
                    subtitle_bottom: 'Короткий путь к успеху в Кэндо для взрослых и детей ',
                    buttonText: 'Подробности',
                    link: '/'
                }],


                titlePromoGoToTraining: [{
                    img: '/img/about/image2.jpg ',
                    title: 'ПЕРВЫЕ ШАГИ НА ПУТИ К МАСТЕРСТВУ',
                    subtitle_bottom: 'Курс базовой фехтовальной подготовки.',
                    buttonText: 'ЗАПИСАТЬСЯ НА ТРЕНИРОВКУ',
                    link: '/'
                }],

                ListBlockTitle: [{
                    subtitle: 'Подзаголовок',
                    title: 'Заголовок'
                }],

                ListBlockData: [{
                        icon: '1',
                        title: 'Кому можно заниматься?',
                        text: 'всем, кто достиг 7 лет, независимо от пола и физических кондиций.',
                    },
                    {
                        icon: '2',
                        title: 'Как проходят занятия?',
                        text: 'в зале несколько раз в неделю. Длительность одной тренировки в среднем 1,5-2 часа.',
                    },
                    {
                        icon: '3',
                        title: 'Что нужно для занятий?',
                        text: 'спортивная одежда без обуви. После прохождения базового курса фехтовальной подготовки для дальнейших занятий вам понадобится свой бамбуковый клинок синай (обязательно) и защитный комплект богу (рекомендуется).',
                    },
                ],
            }
        }
    }
</script>