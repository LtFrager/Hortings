<template>
  <div>
    <main-slider :data="topSliderData" />

    <!-- <div class="promo-cards__block">
      <promo-cards :data="promoData" />
    </div> -->

    <div class="mainvideo">
      <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
        <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle"> Хортінг Фехтування у
          школі</span>

      </h2>
      <div>
        <iframe class="video" src="https://www.youtube.com/embed/ZZp4wfeMKe0" frameborder="0"
          allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
    </div>
    <!-- <text-block :data="textBlockAboutUs" /> 

    <title-promo :data="titlePromoData_1" /> 

     <text-block :data="textBlockOurBenefits" />

    <title-promo :data="titlePromoData_2" /> -->

    <!-- <v-parallax style="height:auto" src="/img/about/image4.jpg">
      <v-container>
        <v-layout row justify-end align-center fill-height>
          <v-flex xs12 sm7 md6>
            <list-block :data="ListBlockData" :titleData="ListBlockTitle" />
          </v-flex>
        </v-layout>
      </v-container>
    </v-parallax> -->

    <v-container>
      <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
        <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">КОРИСНА
          ІНФОРМАЦІЯ</span>
        НОВИНИ
      </h2>
      <news :data="newsData" />

      <!-- <h2 data-aos="fade-down" data-aos-duration="1000" class="std__title text__black text-xs-center">
        <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">События</span>
        Ближайшие События
      </h2> 
      <news :data="newsData" /> -->
    </v-container>

  </div>
</template>
<script>
  import MainSlider from '@/components/main/MainSlider'
  import TitlePromo from '@/components/TitlePromo'
  import PromoCards from '@/components/PromoCards'
  import ListBlock from '@/components/ListBlock'
  import TextBlock from '@/components/TextBlock'
  import News from '@/components/News'
  export default {
    components: {
      MainSlider,
      PromoCards,
      TitlePromo,
      ListBlock,
      TextBlock,
      News
    },
    data() {
      return {
        topSliderData: [{
            img: '/img/news-slider/2.jpg',
            orangeTitle: 'ХОРТИНГ',
            title: 'ФЕХТУВАННЯ',
            text: 'Новітній український спорт з давньою традицією.',
            link: '',
            videoSrc: '',
          },
          // {
          //   img: '/img/news-slider/1.jpg',
          //   orangeTitle: 'ХОРТИНГ',
          //   title: 'ФЕХТУВАННЯ',
          //   text: 'розвиває логіку та стратегічне мислення',
          //   link: ''
          // },
          //   {
          //   img: '/img/news-slider/1.jpg',
          //   orangeTitle: 'ХОРТИНГ',
          //   title: 'ФЕХТУВАННЯ',
          //   text: 'це видовищне та яскраве спортивне шоу!',
          //   link: ''
          // },
        ],

        promoData: [{
            img: '/img/index/promo/page-image1.jpg',
            link: '/sections/kendo',
            category: 'Секция',
            title: 'Kendo',
            text: 'Кэндо - это  японское традиционное спортивное фехтование на бамбуковых клинках.',
          },
          {
            img: '/img/index/promo/page-image2.jpg',
            link: '/sections/horting',
            category: 'Секция',
            title: 'Horting Fencing',
            text: 'Хортинг фехтование - это новый вид спорта Украины представляющий из себя контактное единоборство, сочетающее в себе фехтование на клинках сабельного типа с элементами рукопашной борьбы хортинг.',
          },
          {
            img: '/img/index/promo/page-image3.jpg',
            link: '/sections/gladiatoria',
            category: 'Секция',
            title: 'Art of Gladiatoria',
            text: 'Art of Gladiatoria - фехтовальная система, в которой применяются передовые научные разработки в сочетании с древними традициями и знаниями школ фехтования со всего мира!',
          },
        ],

        textBlockAboutUs: [{
          textLeft: false,
          img: '/twstimg.jpg',
          subtitle_top: 'Club Gladiatoria',
          title: 'О НАС',
          boldText: '',
          paragrafs: [
            'Club Gladiatoria - объединяет энтузиастов и любителей искусства фехтования различным стилями фехтования.',
            'Зачем мы фехтуем?',
            'Затем, чтобы соединить человека и клинок с помощью древних знаний и современной науки и наилучшим образом раскрыть и реализовать заложенный в них потенциал!'
          ]
        }],

        textBlockOurBenefits: [{
          textLeft: true,
          img: '/img/index/index3.jpg',
          subtitle_top: 'НАШИ ПРЕИМУЩЕСТВА',
          title: 'С НАМИ ВОЗМОЖНО ВСЁ',
          boldText: '',
          paragrafs: [
            'Принято считать, что любое искусство фехтования, это сложная наука, на изучение которой необходимо потратить долгие годы… ',
            'Так оно и было. Раньше.',
            'Нами разработана уникальная система подготовки, благодаря которой можно освоить любой вид фехтования в кратчайшие сроки. Вы ощутите результат сразу, а не по прошествии долгих месяцев или лет!',
            'Более того, пройдя Курс базовой фехтовальной подготовки, вы будете четко знать, каким именно стилем фехтования вы хотите заниматься больше всего и вольны выбрать направление. Или заниматься во всех наших секциях одновременно! Решать вам. ;)'
          ]
        }],

        ListBlockTitle: [{
          subtitle: 'Club Gladiatoria',
          title: 'Наши условия'
        }],

        ListBlockData: [{
            icon: '1',
            title: 'групповые тренировки ',
            text: 'основная форма тренировочного процесса как для новичков так и для опытных фехтовальщиков, ведь фехтовать в одиночку невозможно.',
          },
          {
            icon: '2',
            title: 'индивидуальные занятия с тренером ',
            text: 'отличное решение для углубленного изучения техник под руководством опытного наставника.',
          },
          {
            icon: '3',
            title: 'личные достижения',
            text: 'участие в семинарах, аттестациях и соревнованиях - как внутри страны, так и за ее пределами.',
          },
        ],

        titlePromoData_1: [{
          img: '/img/index/index4.jpg ',
          title: 'ХОТИТЕ УЗНАТЬ О НАС БОЛЬШЕ',
          subtitle_top: ' Мы - профессиональная и дружная команда ',
          subtitle_bottom: 'Детальная информация о клубе гладиатория',
          buttonText: 'о нас',
          link: '/about-us'
        }],

        titlePromoData_2: [{
          img: '/img/index/index4.jpg ',
          title: 'КУРС БАЗОВОЙ ФЕХТОВОЛЬНОЙ ПОДГОТОВКИ',
          subtitle_top: 'первые шаги на пути к мастерству',
          subtitle_bottom: '',
          buttonText: '',
          link: ''
        }],

        titlePromoGoToTraining: [{
          img: '/img/about/image2.jpg ',
          title: 'ПЕРВЫЕ ШАГИ НА ПУТИ К МАСТЕРСТВУ',
          subtitle_bottom: 'Курс базовой фехтовальной подготовки.',
          buttonText: 'ЗАПИСАТЬСЯ НА ТРЕНИРОВКУ',
          link: '/'
        }],

        newsData: [{
            id: 9,
            tags: ['all', 'annonce'],
            tagname: ['анонс'],
            img: '/img/about-horting/1.jpg',
            date: '16.10.2020 - 18.10.2020',
            title: 'ВСЕУКРАЇНСЬКИЙ СЕМІНАР ДЛЯ ІНСТРУКТОРІВ З ХОРТИНГ ФЕХТУВАННЯ',
            link: '/news/temp9',
            text: 'ГО “Національна федерація хортинг фехтування України”, в рамках договору про співпрацю між ГО “НФХФУ” та Кафедрою спеціальних дисциплін та організації професійної підготовки НУДФСУ, анонсує проведення Всеукраїнського семінару для інструкторів з хортинг фехтування.',
          },
          {
            id: 8,
            tags: ['all', 'event'],
            tagname: ['захід'],
            img: '/img/tempnews/temp8.jpg',
            date: '01.08.2020',
            title: '8-й Міжнародний мотофестиваль «Дорога на СІЧ».',
            link: '/news/temp8',
            text: 'Показові виступи представників Національної федерації хортинг фехтування України в рамках 8-го Міжнародного мотофестивалю «Дорога на СІЧ». Місто Черкаси, Україна, 01.08.2020 р.',
          },
          {
            id: 7,
            tags: ['all', 'event'],
            tagname: ['захід'],
            img: '/img/tempnews/temp_kaf.jpg',
            date: '',
            title: '',
            link: '/news/temp7',
            text: '',
          },
        ],
      }
    }
  }
</script>
<style lang="scss" scoped>
  .promo-cards__block {
    position: relative;
    top: -80px;

    @media screen and (max-width: 600px) {
      top: 0px;
    }
  }

  .mainvideo {
    margin: auto;
    max-width: 720px;

    div {
      height: 0;
      padding-top: 55%;
      position: relative;

      .video {
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
      }
    }
  }
</style>