<template>
    <div>
          <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                    class="subtitle"></span>
                КЕРІВНИЦТВО
            </h2>

         <promo-cards :data="ourPhotos1" />

             <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                    class="subtitle"></span>
               ПОЧЕСНІ ЧЛЕНИ ФЕДЕРАЦІЇ
            </h2>

         <promo-cards :data="ourPhotos2" />

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
                ourPhotos1: [{
                        img: '/img/governance/pres_faleev.png',
                        link:'',
                        category: 'Президент НФХФУ',
                        title: 'Фалєєв Роман Геннадійович ',
                        text: '',
                    },
                    {
                        img: '/img/governance/pres_zinchenko.jpg',
                        link:'',
                        category: 'Віце-президент НФХФУ',
                        title: 'Зінченко Валерій Олександрович',
                        text: '',
                    },
                   {
                        img: '/img/governance/rog2.jpg',
                        link:'',
                        category: 'Віце-президент НФХФУ',
                        title: 'РОГ МАКСИМ ВІКТОРОВИЧ',
                        text: '',
                    },
                        {
                        img: '/img/governance/sakseev.jpg',
                        link:'',
                        category: 'Перший Віце-президент НФХФУ',
                        title: 'Саксєєв Сергій Васильович',
                        text: '',
                    },
                    {
                        img: '/img/governance/pres_havrilyak.jpg',
                        link:'',
                        category: 'Представник НФХФУ у Закарпатській області',
                        title: 'Гавриляк Емеріх Емеріхович',
                        text: '',
                    },
                ],
                ourPhotos2: [{
                        img: '/img/governance/pochet_eremenko.jpg',
                        link:'',
                        category: '',
                        title: 'Єрьоменко Едуард Анатолійович',
                        text: '',
                    },
                    {
                        img: '/img/governance/pochet_kuzora.jpg',
                        link:'',
                        category: '',
                        title: 'КУЗОРА ІВАН ВАСИЛЬОВИЧ',
                        text: '',
                    },
                   {
                        img: '/img/governance/pochet_raevsky.jpg',
                        link:'',
                        category: '',
                        title: 'Раєвський Сергій Віссаріонович',
                        text: '',
                    },
                ],
            }
        }
    }
</script>