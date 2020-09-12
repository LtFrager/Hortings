<template>
    <v-container>
        <h2 data-aos="zoom-in" data-aos-duration="1000" data-aos-delay="300"
            class="std__title text__black text-xs-center">
            <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle"></span>
            Новости
        </h2>
        <filter-gallery :news="newsData" :filterData="filterData" />
    </v-container>
</template>
<script>
    import FilterGallery from "@/components/FilterGallery"
    export default {
        components: {
            FilterGallery
        },
        data() {
            return {
                filterData: [{
                        id: 1,
                        tag: 'all',
                        name: 'Усі новини'
                    },
                    {
                        id: 2,
                        tag: 'annonce',
                        name: 'Анонсы'
                    },
                    {
                        id: 3,
                        tag: 'event',
                        name: 'Заходи'
                    },
                ],
                newsData: [
                     {
                        id: 9,
                        tags: ['all', 'annonce'],
                        tagname: ['анонс'],
                        img: '/img/about-horting/1.jpg',
                        date: '16.10.2020 - 18.10.2020',
                        title: 'ВСЕУКРАЇНСЬКИЙ СЕМІНАР ДЛЯ ІНСТРУКТОРІВ З ХОРТИНГ ФЕХТУВАННЯ',
                        link: '/news/temp9',
                        text: 'ГО “Національна федерація хортинг фехтування України”, в рамках договору про співпрацю між ГО “НФХФУ” та Кафедрою спеціальних дисциплін та організації професійної підготовки НУДФСУ, анонсує проведення Всеукраїнського семінару для інструкторів з хортинг фехтування.',
                    },
                        {
                        id: 8,
                        tags: ['all', 'event'],
                        tagname: ['захід'],
                        img: '/img/tempnews/temp8.jpg',
                        date: '01.08.2020',
                        title: '8-й Міжнародний мотофестиваль «Дорога на СІЧ».',
                        link: '/news/temp8',
                        text: 'Показові виступи представників Національної федерації хортинг фехтування України в рамках 8-го Міжнародного мотофестивалю «Дорога на СІЧ». Місто Черкаси, Україна, 01.08.2020 р.',
                    },
                    {
                        id: 7,
                        tags: ['all', 'event'],
                        tagname: ['захід'],
                        img: '/img/tempnews/temp_kaf.jpg',
                        date: '',
                        title: '',
                        link: '/news/temp7',
                        text: '',
                    },
                    {
                        id: 6,
                        tags: ['all', 'event'],
                        tagname: ['захід'],
                        img: '/img/tempnews/temp6.jpg',
                        date: '24.02.2020',
                        title: 'День Героїв Небесної Сотні',
                        link: '/news/temp6',
                        text: 'До цієї дати пройшов військово-патріотичний захід Федерації хортинг фехтування у Печерській гімназії № 75. ...',
                    },
                    {
                        id: 5,
                        tags: ['all', 'event'],
                        tagname: ['захід'],
                        img: '/img/tempnews/temp5.jpg',
                        date: '12.02.2020',
                        title: 'ХОРТИНГ ФЕХТУВАННЯ в Університетському коледжі Київського університету імені Бориса Грінченка',
                        link: '/news/temp5',
                        text: '12.02.2020 р. в межах програми «Захист Вітчизни» (розділ «Прикладна фізична підготовка, самозахист»), студенти 1 курсу Університетського коледжу ...',
                    },
                    {
                        id: 4,
                        tags: ['all', 'annonce'],
                        tagname: ['анонс'],
                        img: '/img/about-horting/1.jpg',
                        date: '27–29 березня, 2020',
                        title: ' ПЕРШИЙ СЕМІНАР ДЛЯ ІНСТРУКТОРІВ З ХОРТИНГ ФЕХТУВАННЯ У МІСТІ КАМ’ЯНСЬКЕ',
                        link: '/news/temp4',
                        text: '',
                    },
                    {
                        id: 3,
                        tags: ['all', 'event'],
                        tagname: ['захід'],
                        img: 'http://kubg.edu.ua/images/phocagallery/Podii/2019/12_12_fzfvs/12_12_fzfvs_09.jpg',
                        date: '12.12.2019',
                        title: 'Презентація ХОРТИНГ ФЕХТУВАННЯ',
                        link: '/news/temp3',
                        text: 'Презентація ХОРТИНГ ФЕХТУВАННЯ в рамках VІІ Всеукраїнської науково-практичнаої конференціяї «Фізичне виховання, спорт та здоров’я людини: досвід, проблеми, перспективи» ...',
                    },
                    {
                        id: 2,
                        tags: ['all', 'event'],
                        tagname: ['захід'],
                        img: '/img/tempnews/1.jpg',
                        date: '11.11.2019',
                        title: 'ХОРТИНГ ФЕХТУВАННЯ у Національному університеті державної фіскальної служби України',
                        link: '/news/temp1',
                        text: '11 грудня 2019 року у стінах Національного університету державної фіскальної служби України пройшла презентація ХОРТИНГ ФЕХТУВАННЯ ...',
                    },
                    {
                        id: 1,
                        tags: ['all', 'event'],
                        tagname: ['захід'],
                        img: 'http://kam.gov.ua/ua/osximage/pg/190819190982147_p13_2m/pic.jpg',
                        date: '18.08.2019',
                        title: '«Фестиваль здорового способу життя» у місті Кам’янське',
                        link: '/news/temp2',
                        text: '18 серпня у Кам’янському за підтримки міського голови Андрія Білоусова НФХФУ прийняла участь у спортивному святі, яке об’єднало більше 20-ти популярних видів спорту – «Фестиваль здорового способу життя». ...',
                    },
                ],
            }
        }
    }
</script>