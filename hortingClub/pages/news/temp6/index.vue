<template>
    <v-container class="news">
        <h2 class="std__title text__black">
            <span class="subtitle">{{news.date}}</span>
            {{news.title}}
        </h2>

        <div>
            <img src="/img/tempnews/temp6.jpg" alt="img">
            <p class="std__text">
                День Героїв Небесної Сотні — пам'ятний день, що відзначається в Україні 20 лютого на вшанування подвигу
                учасників Революції гідності та увічнення пам'яті Героїв Небесної Сотні.
            </p>
            <p class="std__text">До цієї дати пройшов військово-патріотичний захід Федерації хортинг фехтування у
                Печерській гімназії № 75. Перед учнями 9-11 класів виступив учасник Революції гідності Костянтин Хімчак
                – iнструктор з хортинг фехтования. Свою майстерність у володінні козацькою зброєю продемонстрували
                ветерани АТО – представники Федерації хортинг фехтування. Учні гімназії взяли участь у практичній
                частині заходу, отримавши базові навички володіння козацькою шаблею.

                <p class="std__text">
                    Дякуємо за довіру
                </p>

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