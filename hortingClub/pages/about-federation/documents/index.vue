<template>
    <v-container>
        <h2 data-aos="zoom-in" data-aos-duration="1000" data-aos-delay="300"
            class="std__title text__black text-xs-center">
            <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">Скачать</span>
            Документы
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
                        name: 'All'
                    },
                    {
                        id: 2,
                        tag: 'tag1',
                        name: 'tag1'
                    },
                    {
                        id: 3,
                        tag: 'tag2',
                        name: 'tag2'
                    },
                ],
                newsData: [{
                        id: 1,
                        tags: ['all', 'tag1'],
                        img: '/img/index/news/img1.jpg',
                        date: 'Feb 11, 2019',
                        title: 'WHAT DOES DISCIPLINE LOOK LIKE?',
                        link:'',
                         download: '/img/index/news/img1.jpg',
                        text: 'Most of us can agree that discipline is one of the most ...',
                    },
                    {
                        id: 2,
                        tags: ['all', 'tag1'],
                        img: '/img/index/news/img1.jpg',
                        date: 'Feb 11, 2019',
                        title: 'WHAT DOES DISCIPLINE LOOK LIKE?',
                        link:'',
                          download: '/img/index/news/img1.jpg',
                        text: 'Most of us can agree that discipline is one of the most ...',
                    },
                    {
                        id: 3,
                        tags: ['all', 'tag2'],
                        img: '/img/index/news/img1.jpg',
                        date: 'Feb 11, 2019',
                        title: 'WHAT DOES DISCIPLINE LOOK LIKE?',
                        link:'',
                          download: '/img/index/news/img1.jpg',
                        text: 'Most of us can agree that discipline is one of the most ...',
                    },
                ],
            }
        }
    }
</script>
