<template>
    <v-layout row wrap justify-center>
        <v-flex xs12 sm6 md4 lg3 v-for="(item,i) in data" :key="i">
            <v-card data-aos="flip-left" data-aos-duration="1000" data-aos-delay="500" hover class="cert__item">
                <div class="item__img" :style="'background-image:url(' + item.img +')'">
                    <!-- <nuxt-link :to="item.link" class="item__img-link">
                    </nuxt-link> -->
                </div>
                <v-card-text>
                      <h6 class="item__date">
                        {{item.date}}
                    </h6>
                    <h3 class="item__title">
                            {{item.title}}
                    </h3>
                    <v-card-actions>
                        <v-spacer></v-spacer>
                        <nuxt-link :to="item.link" class="item__arrow-link">
                            Download
                        </nuxt-link>
                    </v-card-actions>
                </v-card-text>
            </v-card>
        </v-flex>
    </v-layout>
</template>

<script>
    export default {
        props: ['data']
    }
</script>

<style lang="scss" scoped>
    .cert__item {
        cursor: default;
        margin: 12px;

        @media screen and (max-width: 768px) {
            margin: 4px;
        }

        @media screen and (max-width: 600px) {
            margin: 8px;
        }

        .item__img {
            padding-top: 120%;
            background-position: top center;
            background-size: cover;
            position: relative;

            // .item__img-link {
            //     position: absolute;
            //     width: 100%;
            //     height: 100%;
            //     background: none;
            // }
        }

        .item__date {
            color: #FBBC04;
            font-size: 12px;
            line-height: 18px;
            font-weight: 400;
        }

        .item__arrow-link {
            color: #FBBC04;
            text-decoration: none;
            font-size: 14px;
            transition: 1s;

            &:hover {
                color: #232a35;
                font-weight: 700;
                transition: .3s;
            }
        }
    }
</style>