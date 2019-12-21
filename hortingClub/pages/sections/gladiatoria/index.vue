<template>
    <div>
        <text-block :data="textBlockGladiatoria" />

        <v-container>
            <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                    class="subtitle">Gladiatoria</span>
                Чем Art of Gladiatoria отличается от других стилей и направлений фехтования:
            </h2>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">
                В Art of Gladiatoria мы стараемся приблизить наше фехтование к реальному бою – поэтому наше фехтование
                «боевое»;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Но уделяем большое внимание технике
                безопасности
                и
                легальности – поэтому оно всё-таки «условное»;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Мы не замыкаемся на фехтовании по
                определённым
                правилам или на технике средневековых трактатов;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Но и не замыкаемся внутри себя – с
                удовольствием
                спаррингуем с представителями других школ;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Наша цель – гармоничное развитие;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Поэтому наша техника не заточена под
                какие-либо
                турнирные правила – хотя, желающие участвуют в турнирах и занимают призовые места;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">о участие в турнирах совсем не обязательно
                –
                прежде
                всего мы занимаемся для себя;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Разработанный нами Курс базовой
                фехтовальной
                подготовки закладывает основы для фехтования любым оружием;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Затем боец специализируется на выбранных им
                типах
                оружия, причём изучает не только технику, но и тактику;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Большое внимание уделяется специальной
                физической
                подготовке, разработанной специально для занимающихся фехтованием и компенсации специфических нагрузок,
                которым
                подвергается организм фехтовальщика;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Параллельно наша система физической
                подготовки
                улучшает осанку и поднимает общую координацию движений – при этом, занимающийся не превращается в
                «качка»;
            </p>
            <p class="std__text" data-aos="fade-up" data-aos-duration="1000">Индивидуальный подход – базовая программа
                общая,
                но
                каждый проходит её в своём темпе, в зависимости от способностей и частоты посещения тренировок, и потом
                специализируется на выбранном оружии;
                А потому Art of Gladiatoria могут заниматься все! Буквально ВСЕ, в том числе и люди с ограниченными
                возможностями
                опрно-двигательного аппарата.
            </p>
        </v-container>

          <title-promo :data="titlePromoFencingForAll" />

         <text-block :data="textBlockFencingForAll" />


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
                textBlockGladiatoria: [{
                    textLeft: true,
                    img: '/img/index/index3.jpg',
                    subtitle_top: 'Gladiatoria',
                    title: 'ART OF GLADIATORIA',
                    boldText: '',
                    paragrafs: [
                        'Art of Gladiatoria - или “условно-боевое фехтование” - это самостоятельное направление в фехтовальном искусстве, позволяющее изучать работу с любым холодным оружием и выполняющими его функции предметами, а специализация на конкретном виде оружия только шлифует полученные навыки.',
                        'Главной особенностью Art of Gladiatoria является применение специальных полимерных клинков (в сочетании со специальной защитной экипировкой) в качестве основного оружия для занятий - как наиболее эффективную на сегодняшний день альтернативу стальному боевому и тренировочному холодному оружию.',
                    ]
                }],

                titlePromoFencingForAll: [{
                    img: '/img/about/image2.jpg ',
                    subtitle_top: 'art of gladiatoria',
                    title: 'ФЕХТОВАНИЕ ДЛЯ ВСЕХ',
                    subtitle_bottom: ''
                }],

                         textBlockFencingForAll: [{
                    textLeft: false,
                    img: '/img/index/index1.jpg',
                    subtitle_top: 'ЗАНЯТИЯ ФЕХТОВАНИЕМ ЛЮДЕЙ С ОГРАНИЧЕННЫМИ ВОЗМОЖНОСТЯМИ',
                    title: '',
                    boldText: 'Методика фехтовальной подготовки Art of Gladiatoria позволяет:',
                    paragrafs: [
                        '',
                        '',
                        '- улучшить моторику и координацию движений;',
                        '- оптимизировать согласованность работы опорно-двигательного аппарата с корой головного мозга;',
                        '- снимать хроническое мышечное перенапряжение,  стресс;',
                        '- предупреждать деградацию мышечных и тканей и суставов;',
                        '- развить выносливость и укрепить сердечно-сосудистую систему;',
                        '- компенсировать функциональные ограничения;',
                        '- выработать индивидуальный стиль фехтования с учетом физиологических особенностей;',
                        '- участвовать в поединках и турнирах наравне со всеми!',
                    ]
                }],

                titlePromoData_2: [{
                    img: '/img/about/image2.jpg ',
                    title: ' ART OF GLADIATORIA',
                    subtitle_bottom: ''
                }],

                titlePromoGoToTraining: [{
                    img: '/img/about/image2.jpg ',
                    title: 'ПЕРВЫЕ ШАГИ НА ПУТИ К МАСТЕРСТВУ',
                    subtitle_bottom: 'Курс базовой фехтовальной подготовки.',
                    buttonText: 'ЗАПИСАТЬСЯ НА ТРЕНИРОВКУ',
                    link: '/'
                }],


            }
        }
    }
</script>