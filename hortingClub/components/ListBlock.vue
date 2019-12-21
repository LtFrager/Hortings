<template>
    <div class="padding">
        <div class="my-card">
            <h2 data-aos="fade-left" data-aos-duration="600" class="std__title text__black"
                v-for="(item,i) in titleData" :key="i">
                <span data-aos="fade-down" data-aos-delay="500" data-aos-duration="1000"
                    class="subtitle">{{item.subtitle}}</span>
                {{item.title}}
            </h2>

            <ul class="promo__list">
                <li data-aos="fade-up" data-aos-duration="1000" data-aos-delay="200" v-for="(item,i) in data" :key="i">
                    <div>
                        <div class="list__icon">
                            {{item.icon}}
                        </div>
                    </div>
                    <div class="list__text">
                        <p class="text__black std__text">{{item.title}}</p>
                        <p class="std__text">{{item.text}}</p>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
    export default {
        props: ['data', 'titleData']
    }
</script>

<style lang="scss" scoped>
    .my-card {
        background: rgba(255, 255, 255, .9);
        box-shadow: 0px 3px 1px -2px rgba(0, 0, 0, 0.2), 0px 2px 2px 0px rgba(0, 0, 0, 0.14), 0px 1px 5px 0px rgba(0, 0, 0, 0);
        padding: 8px;
        color: #333;
    }

    .promo__list {
        padding: 0px;
        list-style-type: none;

        li {
            display: flex;
            margin-bottom: 36px;

            .list__icon {
                background: #FBBC04;
                color: white;
                font-size: 36px;
                -webkit-border-radius: 50%;
                -moz-border-radius: 50%;
                border-radius: 50%;
                line-height: 82px;
                height: 82px;
                width: 82px;
                margin-right: 30px;
                text-align: center;
            }

            .list__text {
                // display: flex;

                .text__black {
                    text-transform: uppercase;
                    margin: 0px;
                }
            }
        }
    }

    .padding {
        padding: 50px 0px 10px;
    }
</style>