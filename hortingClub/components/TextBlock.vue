<template>
  <div>
    <v-parallax v-for="(item,i) in data" :key="i" style="height:auto;min-height:450px;" :src="item.img">
      <v-container>
        <v-layout class="padding" row align-center fill-height
          v-bind:class="[item.textLeft ? 'justify-start' : 'justify-end']">
          <v-flex xs12 sm8 md6 class="my-card">
            <h2 data-aos="fade-left" data-aos-duration="600" class="std__title text__black">
              <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000"
                class="subtitle">{{item.subtitle_top}}</span>
              {{item.title}}
            </h2>
            <p data-aos="fade-up" data-aos-duration="1000" class="text__black std__text"> {{item.boldText}} </p>
            <p v-for="(item,i) in item.paragrafs" :key="i" data-aos="zoom-in-up" data-aos-duration="1200" class="std__text">
              {{item}}
            </p>
          </v-flex>
        </v-layout>
      </v-container>
    </v-parallax>
  </div>
</template>
<script>
  export default {
    props: ['data']
  }
</script>

<style lang="scss" scoped>
  .padding {
    padding: 40px 0px 20px;
  }
  .subtitle{
    text-transform: uppercase;
  }
  p{
    margin-bottom: 8px;
  }
  .my-card{
    background: rgba(255,255,255,.9);
    box-shadow: 0px 3px 1px -2px rgba(0, 0, 0, 0.2), 0px 2px 2px 0px rgba(0, 0, 0, 0.14), 0px 1px 5px 0px rgba(0, 0, 0, 0);
    padding: 8px;
    color: #333;
  }
</style>