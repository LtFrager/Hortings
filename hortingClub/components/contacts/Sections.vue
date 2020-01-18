<template>
    <v-container>
        <v-layout row wrap>
            <v-flex xs12 sm6 md4 v-for="(item ,i) in data" :key="i" style="padding: 0 6px;">
                <h3 class="section_list-city">{{item.cityName}}</h3>
                <ul class="section_list">
                    <li class="section_list-item" v-for="(item ,i) in item.citySections" :key="i">
                        <!-- <v-menu transition="scroll-y-transition">
                                <template v-slot:activator="{ on }"> -->
                        <!-- <p v-on="on" style="cursor:pointer"> -->
                        {{item.sectionName}}
                        <!-- </p> -->
                        <!-- </template> -->
                        <ul class="list_item-descr_list" v-for="(item ,i) in item.sectionsDescr" :key="i">
                            <li class="descr-item" v-for="(item ,i) in item.sectionPhone" :key="i">
                                <a :href="'tel:' + item">{{item}}</a>
                            </li>
                            <li class="descr-item" v-for="(item ,i) in item.sectionEmail" :key="i">
                                <a :href="'mailto:' + item">{{item}}</a>
                            </li>
                            <li class="descr-item">
                                <a :href="item.sectionAdress[0]">{{item.sectionAdress[1]}}</a>
                            </li>
                        </ul>
                        <!-- // </v-menu> -->
                    </li>
                </ul>
            </v-flex>
        </v-layout>
    </v-container>
</template>
<script>
    export default {
        props: ['data']
    }
</script>
<style lang="scss" scoped>
    .section_list-city {
        font-size: 24px;
        font-weight: 800;
        margin-top: 12px;
        margin-bottom: 12px;
    }

    .section_list {
        padding: 0;
        list-style-type: none;

        .section_list-item {
            text-transform: uppercase;
            font-size: 16px;
            line-height: 1;
            font-weight: 400;
            color: #232a35;
            letter-spacing: 3px;
            margin-bottom: 24px;
        }
    }

    .v-menu__content {
        min-width: 200px !important;
        width: fit-content !important;
        max-width: 100% !important;
        background: #fff !important;
    }

    .list_item-descr_list {
        padding: 6px 8px;

        .descr-item {
            list-style-type: none;

            font-size: 18px;
            line-height: 30px;
            font-weight: 300;
            margin-bottom: 6px;
            letter-spacing: 1px;
            line-height: 1;
            text-transform: none;

            a {
                color: #9f9f9f;
                text-decoration: none;
            }
        }
    }
</style>