<template>
    <div>
        <text-block :data="textBlockHorting" />

        <v-parallax style="height:auto" src="/img/about/image4.jpg">
            <v-container>
                <v-layout row justify-end align-center fill-height>
                    <v-flex xs12 sm8 md7>
                        <list-block :data="ListBlockData" :titleData="ListBlockTitle" />
                    </v-flex>
                </v-layout>
            </v-container>
        </v-parallax>

        <title-promo :data="titlePromoData_2" />

        <v-container>
            <div>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    О сновным принципом Кэндо являетсяединство духа (Ки), меча (Кэн) итела (Тай), что всовременной
                    трактовке соответствует эмоциям и чувствам, интеллекту (мечкаксимвол разума) и телесному
                    здоровью (в том числе моторике, координации и сенсорике). То есть в процессе тренировок
                    происходит
                    гармоничное развитие как физических, так и психологических аспектов личности. Преодолевая
                    кажущееся неразрешеннимым противоречие между духовным и материальным началами современного
                    человека, Кэндо соединяетих в единую систему, позволяя наилучшим образом раскрыть и
                    реализовать
                    заложенный в человеке потенциал.
                </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    We create content that engages and informs, and we complement it with practical tools to make
                    living healthy an easier and sustainable process. We started a tradition when our doors first
                    opened in 2007 of doing introductions at the beginning of each class – a tradition which has been
                    adopted by Sportek gyms all over the country. Also, while many of our workouts are timed and
                    competitive, it is all done in a supportive and team-oriented environment. Welcome!
                </p>

                <img style="max-width:50%;float:left;margin:12px" src="/img/about/trainers/team-1.jpg" alt="img"
                    data-aos="fade-right" data-aos-duration="1000">

                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    There’s nothing better than having your very own coach and mentor. Need an extra push? Our personal
                    trainers are certified experts in exercise physiology, anatomy, training program development,
                    exercise application and fitness assessments. They work for you no matter your age or fitness
                    level.
                </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    The importance of will-power is recognized by most men, yet few deliberately give any time or
                    thought to its development. Why we resist one thing and yield to another may be due to "the
                    strongest motive," but what more particularly concerns us in the study of self-confidence is in
                    what way this mighty power can be built and directed.
                </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    Gym caters for all levels of fitness. Among its most impressive aspects are the variety of classes
                    such as spinning for cardio fitness and Body Pump for burning off the excess weight. The gym
                    instructors are another plus point – professional, knowledgeable, dedicated and friendly. The
                    equipment is all brand new and state of the art.
                </p>
                <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                    The importance of will-power is recognized by most men, yet few deliberately give any time or
                    thought to its development. Why we resist one thing and yield to another may be due to "the
                    strongest motive," but what more particularly concerns us in the study of self-confidence is in
                    what way this mighty power can be built and directed.
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

                textBlockHorting: [{
                    textLeft: true,
                    img: '/img/horting/hort3.jpg',
                    subtitle_top: 'Gladiatoria',
                    title: 'ХОРТИНГ ФЕХТОВАНИЕ',
                    boldText: 'Хортинг фехтование - или “украинский сабельный бой” - это новый вид спорта Украины',
                    paragrafs: [
                        'Это новый вид спорта Украины, который объединяет в себе фехтование на исторических саблях с элементами рукопашной борьбы хортинг.',
                        'В хортинг фехтовании в качестве спортивных снарядов применяются специальные полимерные клинки - “синтсабли”. Данные изделия безопасны и позволяют заниматься полноконтактным фехтованием детям начиная с семи лет.',
                    ]
                }],

                titlePromoData_1: [{
                    img: '/img/about/image2.jpg ',
                    title: 'Большой текст',
                    subtitle_bottom: 'Малый текст, можно добавить кнопку'
                }],

                titlePromoData_2: [{
                    img: '/img/about/image2.jpg ',
                    title: 'Опцыонально',
                    subtitle_bottom: 'Место для кучи текста ниже (можно статью вставить)'
                }],


                    titlePromoGoToTraining: [{
                    img: '/img/about/image2.jpg ',
                    title: 'ПЕРВЫЕ ШАГИ НА ПУТИ К МАСТЕРСТВУ',
                    subtitle_bottom: 'Курс базовой фехтовальной подготовки.',
                        buttonText: 'ЗАПИСАТЬСЯ НА ТРЕНИРОВКУ',
          link: '/'}],

                ListBlockTitle: [{
                    subtitle: 'Преимущества',
                    title: 'Преимуществами полимерных клинков, перед их стальными и прочими аналогами являются:'
                }],

                ListBlockData: [{
                        icon: '1',
                        title: 'Безопасность',
                        text: 'всем, кто достиг 7 лет, независимо от пола и физических кондиций.',
                    },
                    {
                        icon: '2',
                        title: 'Реалистичность',
                        text: 'Максимальная на данный момент приближенность тренировочных полимерных клинков по своим тактико-техническим характеристикам к аналогичному боевому холодному оружию.',
                    },
                    {
                        icon: '3',
                        title: 'Высокая износостойкость и долговечность.',
                        text: '',
                    },
                    {
                        icon: '4',
                        title: ' Доступность и цена.',
                        text: '',
                    },
                    {
                        icon: '5',
                        title: 'Легальность.',
                        text: 'изделия не являются холодным оружием',
                    },
                ],
            }
        }
    }
</script>