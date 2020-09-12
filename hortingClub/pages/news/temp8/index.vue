<template>
    <v-container class="news">

        <h2 class="std__title text__black">
            <span class="subtitle">01.08.2020</span>
            8-й Міжнародний мотофестиваль «Дорога на СІЧ».
        </h2>

        <div>
            <iframe width="100%" height="500px" src="https://www.youtube.com/embed/3WRZdgnnIfc" frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen></iframe>
        </div>

        <button class="std__button" @click="$router.push('/news/')">До новин</button>
    </v-container>
</template>
<script>
    export default {
        data() {
            return {
                news: {
                    img: '/img/tempnews/temp5.jpg',
                    date: '24.02.2020',
                    title: 'День Героїв Небесної Сотні',
                    media: ['/img/index/news/img1.jpg', '/img/index/news/img1.jpg', '/img/index/news/img1.jpg',
                        '/img/index/news/img1.jpg'
                    ]
                }
            }
        }
    }
</script>


<style lang="scss" scoped>
    .news {
        padding-top: 60px;
        padding-bottom: 40px;
        min-height: 80vh;

        p {
            text-indent: 1.5em;
            margin-bottom: 32px;
        }

        img {
            float: left;
            margin-right: 30px;
            margin-bottom: 30px;
            max-width: 50%;

            @media screen and (max-width: 600px) {
                max-width: 100%;
                margin: 0;
                padding-bottom: 12px;
            }
        }

        button {
            margin: auto;
        }
    }
</style>