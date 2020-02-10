<template>
    <div>
          <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                    class="subtitle"></span>
               НАШІ ПАРТНЕРИ
            </h2>

         <promo-cards :data="ourPhotos" />

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
                        img: '/img/partners/chorting_logo_white.jpg',
                        link:'',
                        category: '',
                        title: '',
                        text: 'НАЦІОНАЛЬНА ФЕДЕРАЦІЯ БОЙОВОГО ХОРТИНГУ УКРАЇНИ',
                    },
                    {
                         img: '/img/partners/partners_nalogoviki.jpg',
                        link:'',
                        category: '',
                        title: '',
                        text: 'НАВЧАЛЬНО-НАУКОВИЙ ІНСТИТУТ СПЕЦІАЛЬНОЇ ФІЗИЧНОЇ І БОЙОВОЇ ПІДГОТОВКИ ТА РЕАБІЛІТАЦІЇ ПРИ НУДФСУ',
                    },
                   {
                          img: '/img/partners/udfsu_kafedra_logo2.jpg',
                        link:'',
                        category: '',
                        title: '',
                        text: 'КАФЕДРА СПЕЦІАЛЬНИХ ДИСЦИПЛІН ТА ОРГАНІЗАЦІЇ ПРОФЕСІЙНОЇ ПІДГОТОВКИ НУДФСУ',
                    },
                   {
                          img: '/img/partners/partners_kolodach.jpg',
                        link:'',
                        category: '',
                        title: '',
                        text: 'ВІТЧИЗНЯНИЙ НОЖОВИЙ БРЕНД',
                    },
                        {
                          img: '/img/partners/forge1.jpg',
                        link:'',
                        category: 'СПОРТИВНА ЗБРОЯ ТА ЗАХИСТ ДЛЯ ХОРТИНГ ФЕХТУВАННЯ',
                        title: '',
                        text: 'КУЗНЯ ФАНТАЗІЙ',
                    },
                    // {
                    //       img: '/img/partners/forge1.jpg',
                    //     link:'http://lezo.ua/',
                    //     category: 'СПОРТИВНА ЗБРОЯ ТА ЗАХИСТ ДЛЯ ХОРТИНГ ФЕХТУВАННЯ',
                    //     title: '',
                    //     text: 'КУЗНЯ ФАНТАЗІЙ',
                    // },
                ],
            }
        }
    }
</script>