<template>
    <div>
        <div v-for="(item,i) in data" :key="i">
            <v-parallax style="height:auto" :src="item.img">
                <v-container>
                    <v-layout column justify-center align-center fill-height class="text-xs-center padding">
                        <h2 data-aos="fade-up" data-aos-duration="1000" class="std__title ">
                            <span v-if="item.subtitle_top" class="subtitle" data-aos="fade-down" data-aos-duration="1000" data-aos-delay="200">{{item.subtitle_top}}</span>
                            {{item.title}}
                            <span v-if="item.subtitle_bottom" class="subtitle_bottom" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="200">{{item.subtitle_bottom}}</span>
                        </h2>
                        <p v-if="item.text" class="std__text text_grey" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="400">
                            {{item.text}}
                        </p>
                        <button v-if="item.link" data-aos="fade-up" data-aos-duration="1000" data-aos-delay="600" class="std__button"
                            @click="$router.push(item.link)">{{item.buttonText}}</button>
                    </v-layout>
                </v-container>
            </v-parallax>
        </div>
    </div>
</template>
<script>
    export default {
        props: ['data']
    }
</script>

<style lang="scss" scoped>
    h2 {
        font-size: 60px;
        line-height: 1.2307;
        font-weight: 800px;
        display: flex;
        text-align: center;
        flex-direction: column;
        margin-bottom: 14px;

        @media screen and (max-width: 870px) {
            font-size: 38px;
        }

        .subtitle_bottom {
            font-size: 18px;
            line-height: 1.2307;
            font-weight: 700;
            letter-spacing: 3px;
            margin-bottom: 42px;
        }
    }
    .padding{
    padding: 56px 0px;
}
</style>