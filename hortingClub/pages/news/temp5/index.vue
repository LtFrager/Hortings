<template>
    <v-container class="news">
        <h2 class="std__title text__black">
            <span class="subtitle">{{news.date}}</span>
            {{news.title}}
        </h2>

        <div>
            <img src="/img/tempnews/temp5.jpg" alt="img">
            <p class="std__text">
                12.02.2020 р. в межах програми «Захист Вітчизни» (розділ «Прикладна фізична підготовка, самозахист»),
                студенти 1 курсу Університетського коледжу Київського університету імені Бориса Грінченка мали змогу
                познайомитись із новітнім виду спорту України - хортинг фехтуванням.
            </p>
            <p class="std__text">
                Студенти дізнались про бойові традиції запорізьких козаків, випробували зброю та обладунки тих часів, а
                також взяли участь у тренувальних двобоях з хортинг фехтування вже з сучасною спортивною зброєю та
                спеціальним захисним спорядженням, що дозволяють безпечно для здоров’я проводити спортивний двобій
                максимально наближено до реального історичного бою.
            </p>
            <p class="std__text">
                Завдяки Національній Федерації хортинг фехтування України студенти 1 курсу Університетського коледжу
                Київського університету імені Бориса Грінченка отримали не лише теоретичні, а й практичні базові навички
                із самозахисту зі зброєю та без, як козаки-запоріжці.
            </p>
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
                    date: '12.02.2020',
                    title: 'ХОРТИНГ ФЕХТУВАННЯ в Університетському коледжі Київського університету імені Бориса Грінченка',
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