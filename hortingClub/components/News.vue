<template>
    <v-layout row wrap justify-center>
        <v-flex xs12 sm4 v-for="(item,i) in data" :key="i">
                <news-card :data="item" />
        </v-flex>
    </v-layout>
</template>

<script>
    import NewsCard from "@/components/NewsCard"
    export default {
    props: ['data'],
        components: {
            NewsCard
        }
    }
</script>
