<template>
    <v-container class="news">
        <div>
            <img src="/img/tempnews/temp_kaf.jpg" alt="img">

             <img src="/img/tempnews/kaf2.jpg" alt="img">
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