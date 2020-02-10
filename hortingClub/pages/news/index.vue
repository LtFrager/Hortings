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
                newsData: [{
                        id: 4,
                        tags: ['all', 'annonce'],
                        tagname: ['Анонс'],
                        img: '/flag.jpg',
                        date: 'буде об`явлено',
                        title: 'ПЕРШИЙ СЕМІНАР ДЛЯ ІНСТРУКТОРІВ З ХОРТИНГ ФЕХТУВАННЯ КАМ’ЯНСЬКЕ 2020',
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