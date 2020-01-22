<template>
  <div>
    <main-slider :data="topSliderData" />

    <!-- <div class="promo-cards__block">
      <promo-cards :data="promoData" />
    </div> -->

 
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
        <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">КОРИСНА ІНФОРМАЦІЯ</span>
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
            link: ''
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
            id: 3,
            tags: ['all', 'tag1'],
            tagname: [],
            img: 'http://kubg.edu.ua/images/phocagallery/Podii/2019/12_12_fzfvs/12_12_fzfvs_09.jpg',
            date: '12.12.2019',
            title: 'Презентація ХОРТИНГ ФЕХТУВАННЯ',
            link: '/news/temp3',
            text: 'Презентація ХОРТИНГ ФЕХТУВАННЯ в рамках VІІ Всеукраїнської науково-практичнаої конференціяї «Фізичне виховання, спорт та здоров’я людини: досвід, проблеми, перспективи» ...',
          },
          {
            id: 1,
            tags: ['all', 'tag1'],
            tagname: [],
            img: '/img/tempnews/1.jpg',
            date: '11.11.2019',
            title: 'ХОРТИНГ ФЕХТУВАННЯ у Національному університеті державної фіскальної служби України',
            link: '/news/temp1',
            text: '11 грудня 2019 року у стінах Національного університету державної фіскальної служби України пройшла презентація ХОРТИНГ ФЕХТУВАННЯ ...',
          },
          {
            id: 2,
            tags: ['all', 'tag1'],
            tagname: [],
            img: 'http://kam.gov.ua/ua/osximage/pg/190819190982147_p13_2m/pic.jpg',
            date: '18.08.2019',
            title: '«Фестиваль здорового способу життя» у місті Кам’янське',
            link: '/news/temp2',
            text: '18 серпня у Кам’янському за підтримки міського голови Андрія Білоусова НФХФУ прийняла участь у спортивному святі, яке об’єднало більше 20-ти популярних видів спорту – «Фестиваль здорового способу життя». ...',
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
</style>