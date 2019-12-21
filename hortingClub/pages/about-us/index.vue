<template>
    <div>
       

        <text-block :data="textBlockAboutUs" />


          <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                    class="subtitle">Наша команда</span>
                Наша команда
            </h2>

         <promo-cards :data="ourPhotos" />

        <v-container>
            <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                    class="subtitle">Gladiatoria</span>
                НАШИ ЦЕЛИ И ЗАДАЧИ
            </h2>

            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                Исследование прикладного фехтования клинковым оружием, известного человечеству на протяжении его истории
                (доступного для изучения через сохранившуюся материальную культуру).
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Преодоление редукционизма в небоевых и
                условно
                боевых видах фехтования из-за тактико-технического
                несоответствия характеристик тренировочного/спортивного холодного оружия его боевым и историческим
                аналогам.
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Разработка мер безопасности, оптимизация,
                стандартизация и внедрение средств индивидуальной защиты
                фехтовальщиков для занятий с клинком (как для тренировок так и соревнований).
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Развитие существующих и новых стилей
                фехтования,
                поддержка отдельных фехтовальщиков и
                энтузиастов-исследователей.
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Их объединение на основе Единой теории
                фехтования.
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Научная разработка методик, техник и
                практик по
                условно-прикладному фехтованию клинком.
            </p>

            <p class="std__text" data-aos="fade-up" data-aos-duration="1000"> Разработка понятного для всех “общего
                языка
                фехтования”: Единой теории фехтования.
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Разработка универсальных правил проведения
                и
                судейства спортивных поединков с клинком для
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">организации межстиливых и внутристилевых
                соревнований по фехтованию клинковым холодным оружием из различных
                регионов планеты и исторических эпох.
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Развитие детского спортивного фехтовального
                движения на базе единой теории фехтования в воспитательных,
                оздоровительных и спортивных целях.
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Разработка методик обучения фехтованию
                людей с
                ограниченными возможностями.
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Реализация идеи развития человеческого
                сознания,
                его духовности и нравственности при помощи Искусства (Пути)
                Меча (как в условно-прикладном, так и в его состязательном аспекте).
            </p>
        </v-container>

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
                ourPhotos: [{
                        img: '/img/index/promo/page-image1.jpg',
                        link:'',
                        category: 'Должность',
                        title: 'Имя фамилия',
                        text: 'НЕмного текста (опционально)',
                    },
                    {
                        img: '/img/index/promo/page-image1.jpg',
                        link:'',
                        category: 'Должность',
                        title: 'Имя фамилия',
                        text: 'НЕмного текста (опционально)',
                    },
                   {
                        img: '/img/index/promo/page-image1.jpg',
                        link:'',
                        category: 'Должность',
                        title: 'Имя фамилия',
                        text: 'НЕмного текста (опционально)',
                    },
                ],

                textBlockAboutUs: [{
                    textLeft: true,
                    img: '/img/index/index3.jpg',
                    subtitle_top: 'Gladiatoria',
                    title: ' Club Gladiatoria',
                    boldText: ' Club Gladiatoria - это инициативная группа энтузиастов-исследователей и любителей искусства фехтования клинковым оружием. ',
                    paragrafs: [
                        'Зачем мы исследуем фехтование? ',
                        'Затем, чтобы объединить человека и клинок с помощью современной науки и наилучшим образом раскрыть и реализовать заложенный в них потенциал! ',
                    ]
                }],
               
            }
        }
    }
</script>