<template>
    <v-parallax style="height:auto" src="/img/index/index2.jpg">
        <v-container>
            <div class="our-skils__block">
                <v-layout row column justify-center align-center fill-height>
                    <h2 data-aos="fade-right" data-aos-duration="1000" class="std__title">CHECK OUR SKILLS</h2>
                    <p data-aos="fade-left" data-aos-duration="1000" class="text_grey std__text">
                        We’ve spent over 10 years defining fitness and now we’re reinventing it. Through personalization
                        and
                        innovation, we’ve evolved so that you can transform your life. </p>
                    <v-layout row wrap style="width: 100%;">
                        <v-flex data-aos="fade-up" data-aos-duration="1000" xs12 sm6 md3 class="layout justify-center"
                            v-for="(item,i) in ourSkillsData" :key="i">
                            <div>
                                <div class="our-skils__skill">
                                    {{item.skillNum}}%
                                </div>
                                <div class="std__title">
                                    <span class="subtitle">{{item.skillName}}</span>
                                </div>
                            </div>
                        </v-flex>
                    </v-layout>
                </v-layout>
            </div>
        </v-container>
    </v-parallax>
</template>

<script>
    export default {
        data() {
            return {
                ourSkillsData: [{
                        skillNum: '90',
                        skillName: 'PROFESSIONALISM',
                    },
                    {
                        skillNum: '90',
                        skillName: 'PROFESSIONALISM',
                    },
                ],
            }
        }
    }
</script>
<style lang="scss" scoped>
    .our-skils__block {
        padding: 30px 0px;

        .text_grey {
            margin-bottom: 40px;
            text-align: center;
        }

        .our-skils__skill {
            border-radius: 50%;
            border: 12px solid #FBBC04;
            display: inline-flex;
            font-size: 36px;
            line-height: 66px;
            padding: 32px;
            margin-bottom: 20px;
        }
    }
</style>