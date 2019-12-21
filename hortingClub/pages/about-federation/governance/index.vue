<template>
    <div>
          <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                    class="subtitle">Наша команда</span>
                Руководство
            </h2>

         <promo-cards :data="ourPhotos" />

             <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
                <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                    class="subtitle">Наша команда</span>
                Почётные члены
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
                        img: '/img/index/promo/page-image1.jpg',
                        link:'',
                        category: 'Должность',
                        title: 'Имя фамилия',
                        text: 'НЕмного текста (опционально)',
                    },
                    {
                        img: '/img/index/promo/page-image1.jpg',
                        link:'',
                        category: 'Должность',
                        title: 'Имя фамилия',
                        text: 'НЕмного текста (опционально)',
                    },
                   {
                        img: '/img/index/promo/page-image1.jpg',
                        link:'',
                        category: 'Должность',
                        title: 'Имя фамилия',
                        text: 'НЕмного текста (опционально)',
                    },
                ],
            }
        }
    }
</script>