<template>
    <v-card data-aos="flip-left" data-aos-duration="1000" data-aos-delay="00" hover class="news__item">
        <div class="item__img" :style="'background-image:url(' + data.img +')'">
            <nuxt-link v-if="data.link" :to="data.link" class="item__img-link">
            </nuxt-link>

            <a v-if="data.download" :href="data.download" download class="item__img-link">
            </a>

            <div class="tag-field" v-if="data.tagname">
                <span v-for="(item,i) in data.tagname" :key="i" class="tag-field_tag">{{item}}</span>
            </div>
        </div>
        <v-card-text>
            <h6 class="item__date">
                {{data.date}}
            </h6>
            <h3 class="item__title">
                <nuxt-link :to="data.link">
                    {{data.title}}
                </nuxt-link>
            </h3>
            <p class="text_grey std__text">
                {{data.text}}
            </p>
            <v-card-actions>
                <v-spacer></v-spacer>
                <nuxt-link v-if="data.link" :to="data.link" class="item__arrow-link">
                    Дізнатісь більше
                </nuxt-link>

                <a v-if="data.download" :href="data.download" download class="item__arrow-link">
                    Downoad
                </a>
            </v-card-actions>
        </v-card-text>
    </v-card>

</template>

<script>
    export default {
        props: ['data']
    }
</script>

<style lang="scss" scoped>

     .news__item {
        cursor: default;
        margin: 12px;

        @media screen and (max-width: 768px) {
            margin: 4px;
        }

        @media screen and (max-width: 600px) {
            margin: 8px;
        }

        .item__img {
            height: 0;
            padding-top: 85%;
            background-position: center;
            background-size: cover;
            position: relative;

            .item__img-link {
                position: absolute;
                width: 100%;
                height: 100%;
                background: none;
            }

            .tag-field {
                flex-wrap: wrap-reverse;
                display: flex;
                flex-direction: row-reverse;
                position: absolute;
                bottom: 0;
                right: 0;

                .tag-field_tag {
                    background: #111;
                    color: #FBBC04;
                    padding: 2px 6px;
                    font-size: 12px;
                    display: block;
                    margin: 2px;
                }
            }

        }

        .item__date {
            color: #FBBC04;
            font-size: 12px;
            line-height: 18px;
            font-weight: 400;
        }

        .item__title {

            a {
                text-decoration: none;
                text-transform: uppercase;
                color: #232a35;
                font-size: 18px;
                line-height: 1.2307;
                font-weight: 700;
                transition: 1s;

                &:hover {
                    color: #FBBC04;
                    transition: .3s;
                }
            }
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