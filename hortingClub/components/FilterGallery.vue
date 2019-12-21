<template>
    <v-container>
        <ul class="filter__actions d-flex justify-center">
            <li v-for="(item,i) in filterData" :key="i">
                <button v-bind:class="{selected:item.id == isSelected}"
                    v-on:click="filter(`${item.tag}`),isSelected = item.id">{{item.name}}</button>
            </li>
        </ul>

        <transition-group name="list-complete" class="list-complete" tag="section">
            <v-flex xs12 sm6 md6 lg4 v-for="item in filteredItems" v-bind:key="item.id" class="list-complete-item">
                <!-- <img class="list-complete-img" :src="'http://placehold.it/450x200?text='+item.id" alt="" /> -->

                <v-card data-aos="flip-left" data-aos-duration="1000" data-aos-delay="00" hover class="news__item">
                    <div class="item__img" :style="'background-image:url(' + item.img +')'">
                        <nuxt-link v-if="item.link" :to="item.link" class="item__img-link">
                        </nuxt-link>
                        
                        <a v-if="item.download" :href="item.download" download class="item__img-link">
                        </a>
                    </div>
                    <v-card-text>
                        <h6 class="item__date">
                            {{item.date}}
                        </h6>
                        <h3 class="item__title">
                            <nuxt-link :to="item.link">
                                {{item.title}}
                            </nuxt-link>
                        </h3>
                        <p class="text_grey std__text">
                            {{item.text}}
                        </p>
                        <v-card-actions>
                            <v-spacer></v-spacer>
                            <nuxt-link v-if="item.link" :to="item.link" class="item__arrow-link">
                                Read more
                            </nuxt-link>

                            <a v-if="item.download" :href="item.download" download class="item__arrow-link">
                                Downoad
                            </a>
                        </v-card-actions>
                    </v-card-text>
                </v-card>
            </v-flex>


        </transition-group>

    </v-container>
</template>

<script>
    export default {
        props: ['news', 'filterData'],
        data() {
            return {
                isSelected: 1,
                // FilterData: [{
                //         id: 1,
                //         tag: 'all',
                //         name: 'All'
                //     },
                //     {
                //         id: 2,
                //         tag: 'tag1',
                //         name: 'tag1'
                //     },
                //     ],

                // items: [{
                //         id: 1,
                //         tags: ['all', 'tag1'],
                //         img: '/img/index/news/img1.jpg',
                //         date: 'Feb 11, 2019',
                //         title: 'WHAT DOES DISCIPLINE LOOK LIKE?',
                //         link: '/news/id',
                //    download:'/asd/'
                //         text: 'Most of us can agree that discipline is one of the most ...',
                //     },
                //     {
                //         id: 2,
                //         tags: ['all', 'tag2'],
                //         img: '/img/index/news/img1.jpg',
                //         date: 'Feb 11, 2019',
                //         title: 'WHAT DOES DISCIPLINE LOOK LIKE?',
                //         link: '/news/id',
                //         text: 'Most of us can agree that discipline is one of the most ...',
                //     },
                // ],
                currentTag: 'all'
            }
        },
        computed: {
            filteredItems: function () {
                var filter = this.currentTag;
                return this.news.filter(function (item) {
                    return item.tags.indexOf(filter) !== -1;
                });
            }
        },
        methods: {
            // shuffle: function () {
            //     this.items = _.shuffle(this.items)
            // },
            filter: function (tag) {
                this.currentTag = tag;

            }
        }
    }
</script>


<style lang="scss" scoped>
    .filter__actions {
        padding: 0;
        margin: 0;
        list-style-type: none;
        flex-wrap: wrap;
        margin: auto;
        width: 100%;
        max-width: 620px;

        li {
            padding: 5px;
            text-align: center;

            button {
                background: #FBBC04;
                text-transform: uppercase;
                color: #ffffff;
                border-radius: 4px;
                border: 0px solid transparent;
                font-size: 12px;
                line-height: 30px;
                font-weight: bold;
                letter-spacing: 1px;
                padding: 10px 30px 10px 30px;
                transition: 0.3s;
                outline: none;

                &.selected {
                    background: #232a35;
                    color: #ffffff;
                }

                &:hover {
                    opacity: .7;
                }
            }
        }
    }

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
            height: 220px;
            background-position: center;
            background-size: cover;
            position: relative;

            .item__img-link {
                position: absolute;
                width: 100%;
                height: 100%;
                background: none;
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

    .list-complete {
        display: flex;
        width: 100%;
        flex-direction: row;
        flex-wrap: wrap;
    }

    .list-complete-enter,
    .list-complete-leave-to {
        opacity: 0;
        transform: translateY(30px);
    }

    .list-complete-leave-active {
        position: absolute;
    }
</style>