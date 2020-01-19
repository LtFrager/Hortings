<template>
  <v-app style="background:#fff">
    <div class="navbar">
      <v-container class="layout justify-space-between align-center" style="padding-top:0;padding-bottom:0;">

        <nuxt-link style="text-decoration: none;" to="/">
          <div class="logo-block">
            <img width="100%" src="/logo.png" alt="">
            <h2>Horting <span>Fencing</span></h2>
          </div>
        </nuxt-link>

        <ul class="nav__list hidden-sm-and-down">
          <li v-for="(item,i) in navigationData" :key="i">
            <nuxt-link :to="item.link">
              {{item.title}}
            </nuxt-link>

            <ul class="nav__list-lvl2 hover__list">
              <li v-for="(item,i) in item.chield" :key="i">
                <nuxt-link :to="item.link">
                  {{item.title}}
                </nuxt-link>
              </li>
            </ul>
          </li>
        </ul>

        <v-btn icon dark @click.stop="drawer = !drawer" color="#030409" class="hidden-md-and-up">
          <v-icon>menu</v-icon>
        </v-btn>
      </v-container>
    </div>

    <v-navigation-drawer v-model="drawer" fixed temporary class="mobile-navbar">
      <!-- <v-list class="pt-0" dense>
        <v-list-tile v-for="(item,i) in navigationData" :key="i" @click="$router.push(item.link)" color="#fff">
          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list> -->

      <ul class="nav__list mob-list">
        <li v-for="(item,i) in navigationData" :key="i">
          <nuxt-link :to="item.link">
            {{item.title}}
          </nuxt-link>

          <ul class="nav__list-lvl2 hover__list">
            <li v-for="(item,i) in item.chield" :key="i">
              <nuxt-link :to="item.link">
                {{item.title}}
              </nuxt-link>
            </li>
          </ul>
        </li>
      </ul>

    </v-navigation-drawer>

    <v-content style="padding-top:76px;">
      <nuxt />
    </v-content>

    <footer>
      <!-- <div class="footer__bg">
        <v-container grid-list-xl>
          <v-layout row wrap justify-space-around>
            <v-flex xs12 sm6 md5>
              <h2 class="footer__title">
                ABOUT OUR CLUB
              </h2>
              <p class="footer__text">
                Sportek is a universal gym where everyone becomes an athlete. We work for you to have better shape and
                stronger health!
              </p>
            </v-flex>
            <v-flex xs12 sm6 md3>
              <h2 class="footer__title">
                CONTACT US
              </h2>

              <p class="footer__text">
                4096 N Highland St, Arlington VA 32101, USA<br>
                school@company.com<br>
                800 1234 56 78
              </p>
            </v-flex>
            <v-flex xs12 sm6 md3>
              <h2 class="footer__title">
                QUICK LINKS
              </h2>

              <ul style="padding:none;list-style-type:none;">
                <li style="padding:none; color:#ebebeb;cursor:pointer" v-for="(item,i) in navigationData" :key="i"
                  @click="$router.push(item.link)">
                  {{ item.title }}
                </li>
              </ul>
            </v-flex>
          </v-layout>
        </v-container>
      </div> -->
      <div class="footer__bottom">
        <v-container>
          <p class="copy">
            © 2020 HORTING FENCING®. All rights reserved.
          </p>
        </v-container>
      </div>
    </footer>

    <!-- <my-footer id="contacts" /> -->

  </v-app>
</template>

<script>
  // import MyFooter from '@/components/layouts/MyFooter'
  export default {
    components: {
      // MyFooter
    },
    data() {
      return {
        drawer: null,
        navigationData: [{
            title: 'Головна',
            link: '/'
          },
          {
            title: 'про хф',
            link: '',
            chield: [{
                title: 'ЗАГАЛЬНА ІНФОРМАЦІЯ ',
                link: '/about-horting-fencing/info',
              },
              {
                title: 'СПОРЯДЖЕННЯ ТА ЕКІПИРУВАННЯ ',
                link: '/about-horting-fencing/gear',
              },
              {
                title: 'ПРАВИЛА ЗМАГАНЬ',
                link: '/about-horting-fencing/tournament-rules',
              },
            ]
          },
          {
            title: 'федерація',
            link: '',
            chield: [{
                title: 'ПРО ФЕДЕРАЦІЮ',
                link: '/about-federation/about',
              },
              {
                title: 'КЕРІВНИЦТВО',
                link: '/about-federation/governance',
              },
              {
                title: 'ПАРТНЕРИ',
                link: '/about-federation/partners',
              },
              // {
              //   title: 'ДОКУМЕНТИ',
              //   link: '/about-federation/documents',
              // },
              {
                title: 'ВСТУПИТИ ДО ФЕДЕРАЦІЇ',
                link: '/about-federation/join',
              },
            ]
          },
          {
            title: 'новини',
            link: '/news'
          },
          // {
          //   title: '',
          //   link: '/about-us',
          // },
          // {
          //   title: 'Для теста (не используются)',
          //   link: '',
          //    chield: [{
          //       title: '/news',
          //       link: '/news',
          //     },
          //     {
          //       title: 'filter',
          //       link: '/filter',
          //     },
          //   ]
          // },
          {
            title: 'контакти та представництва',
            link: '/contacts'
          },
        ]
      }
    }
  }
</script>
<style lang="scss" scoped>
  .logo-block {
    display: flex;
    color: #fff;
    max-width: 160px;
    padding: 8px;
    box-sizing: border-box;

    img {
      max-height: 60px;
      width: auto;
    }

    h2 {
      line-height: 20px;
      padding: 5px;

      span {
        font-size: .7em
      }
    }
  }

  .mobile-navbar {
    background: #030409;
    padding-top: 20px;
    //  background: #565169;
  }

  .navbar {
    background: #030409;
    //  background: #565169;
    width: 100%;
    position: fixed;
    z-index: 3;
  }

  .nav__list {
    list-style-type: none;
    display: flex;
    padding: 0px;

    &.mob-list {
      flex-direction: column;

      li {
        padding: 10px;
      }

      .nav__list-lvl2 {
        transform: scale(1);
        position: relative;
      }
    }

    .nav__list-lvl2 {
      padding: 0;
      border-left: 1px solid #FBBC04;
      position: absolute;
      left: 0px;
      width: max-content;
      background: #030409;
    }

    .hover__list {
      transform: scale(0);
      transform-origin: top left;
      transition: .3s;
    }


    li {
      margin-left: 20px;
      position: relative;

      &:hover {
        .hover__list {
          transform: scale(1);
        }
      }

      a {
        color: white;
        text-decoration: none;
        padding: 10px 0;
        font-size: 12px;
        letter-spacing: 1px;
        vertical-align: top;
        text-transform: uppercase;
        transition: 1s;

        &:hover {
          color: #FBBC04;
          transition: 1s;


        }
      }
    }
  }

  .footer__bg {
    background: #232a35;
    font-size: 14px;
    line-height: 24px;

    .footer__title {
      font-size: 16px;
      line-height: 1.2307;
      font-weight: 400;
      color: #b3bbc1;
      font-style: normal;
      letter-spacing: 3px;
      margin-bottom: 26px;
      padding-top: 40px;
    }

    .footer__text {
      font-size: 14px;
      line-height: 24px;
      color: #b3bbc1;
    }
  }

  .footer__bottom {
    background: #1c222b;
    color: #b3bbc1;

    .copy {
      font-size: 14px;
      margin-bottom: 20px;
      margin: 7px 0;
      text-align: right;
    }
  }
</style>


<style lang="scss">
  .std__title {
    font-size: 36px;
    font-weight: 800;
    margin-top: 32px;
    margin-bottom: 32px;
    display: flex;
    flex-direction: column;

    .subtitle {
      font-size: 14px;
      line-height: 1.2307;
      font-weight: 600;
      color: #FBBC04;
      font-style: normal;
      letter-spacing: 2.6px;
    }
  }

  .std__text {
    font-size: 18px;
    line-height: 30px;
    font-weight: 300;
  }

  .text_grey {
    color: #9f9f9f;
  }

  .text__black {
    color: #232a35;
    font-weight: 700;
  }

  .std__button {
    background: #FBBC04;
    text-transform: uppercase;
    color: #ffffff;
    border-radius: 4px;
    border: 0px solid transparent;
    font-size: 12px;
    line-height: 30px;
    font-weight: bold;
    letter-spacing: 1px;
    padding: 10px 30px;
    transition: 0.3s;
    outline: none;

    &:hover {
      background: #232a35;
    }
  }

  * {
    font-family: 'Montserrat', sans-serif;
  }

  @import url('https://fonts.googleapis.com/css?family=Montserrat:100,200,300,400,500,600,700,800,900&subset=cyrillic,cyrillic-ext,latin-ext,vietnamese');
</style>