<template>
    <v-container grid-list-xl>
   
        <v-layout row wrap>
            <v-flex xs12 md6 data-aos="fade-right" data-aos-delay="800" data-aos-duration="1000">
                     <h2 data-aos="fade-right" data-aos-duration="600" class="std__title text__black">
            <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">контакти </span>
          НФХФУ та обласних фед-цій
        </h2>
        <ul class="tab_list layout row wrap" data-aos="slide-right" data-aos-duration="1000">
            <li v-for="(item,i) in  data" :key="i" class="tab"
                @click="myActive = item.active, center = item.position , defZoom=12"
                v-bind:class="{ active:  myActive == item.active }">
                {{item.title}}
            </li>
        </ul>
                <!-- <transition-group name="fade" mode="out-in"> -->
                    <ul class="location_content" v-for="(item,i) in  data" :key="i"
                      v-if="myActive == item.active" >
                        <p class="std__text text_grey">
                            {{item.text}}
                        </p>
                        <li v-for="(item2,i) in item.contactsData" :key="i">
                            <h3 class="location_content_title">
                                {{item2.contacsTitle}}
                            </h3>
                            <p class="std__text text_grey" v-for="(item3,i) in item2.contactsContent" :key="i">
                                {{item3}}
                            </p>
                        </li>
                    </ul>
                <!-- </transition-group> -->
            </v-flex>
            <v-flex data-aos="fade-up" data-aos-delay="800" data-aos-duration="1000">
                <GmapMap class="map-size" v-bind:center="center" v-bind:zoom="defZoom" :options="options">
                    <GmapMarker v-for="(item, index) in  data" v-bind:key="index"
                        v-bind:position="item.position" @click="center=item.position" />
                </GmapMap>
            </v-flex>
        </v-layout>
    </v-container>
</template>
<script>
    export default {
        props:['data'],
        data() {
            return {
                center: {
                    lat: 50.4547,
                    lng: 30.5238
                },
                myActive: 1,
                defZoom:5,
              
                options: {
                    disableDefaultUI: true,
                    // scrollwheel: false,
                    styles: [{
                            "elementType": "geometry",
                            "stylers": [{
                                "color": "#212121"
                            }]
                        },
                        {
                            "elementType": "labels.icon",
                            "stylers": [{
                                "visibility": "off"
                            }]
                        },
                        {
                            "elementType": "labels.text.fill",
                            "stylers": [{
                                "color": "#757575"
                            }]
                        },
                        {
                            "elementType": "labels.text.stroke",
                            "stylers": [{
                                "color": "#212121"
                            }]
                        },
                        {
                            "featureType": "administrative",
                            "elementType": "geometry",
                            "stylers": [{
                                "color": "#757575"
                            }]
                        },
                        {
                            "featureType": "administrative.country",
                            "elementType": "labels.text.fill",
                            "stylers": [{
                                "color": "#9e9e9e"
                            }]
                        },
                        {
                            "featureType": "administrative.land_parcel",
                            "stylers": [{
                                "visibility": "off"
                            }]
                        },
                        {
                            "featureType": "administrative.locality",
                            "elementType": "labels.text.fill",
                            "stylers": [{
                                "color": "#bdbdbd"
                            }]
                        },
                        {
                            "featureType": "poi",
                            "elementType": "labels.text.fill",
                            "stylers": [{
                                "color": "#757575"
                            }]
                        },
                        {
                            "featureType": "poi.park",
                            "elementType": "geometry",
                            "stylers": [{
                                "color": "#181818"
                            }]
                        },
                        {
                            "featureType": "poi.park",
                            "elementType": "labels.text.fill",
                            "stylers": [{
                                "color": "#616161"
                            }]
                        },
                        {
                            "featureType": "poi.park",
                            "elementType": "labels.text.stroke",
                            "stylers": [{
                                "color": "#1b1b1b"
                            }]
                        },
                        {
                            "featureType": "road",
                            "elementType": "geometry.fill",
                            "stylers": [{
                                "color": "#2c2c2c"
                            }]
                        },
                        {
                            "featureType": "road",
                            "elementType": "labels.text.fill",
                            "stylers": [{
                                "color": "#8a8a8a"
                            }]
                        },
                        {
                            "featureType": "road.arterial",
                            "elementType": "geometry",
                            "stylers": [{
                                "color": "#373737"
                            }]
                        },
                        {
                            "featureType": "road.highway",
                            "elementType": "geometry",
                            "stylers": [{
                                "color": "#3c3c3c"
                            }]
                        },
                        {
                            "featureType": "road.highway.controlled_access",
                            "elementType": "geometry",
                            "stylers": [{
                                "color": "#4e4e4e"
                            }]
                        },
                        {
                            "featureType": "road.local",
                            "elementType": "labels.text.fill",
                            "stylers": [{
                                "color": "#616161"
                            }]
                        },
                        {
                            "featureType": "transit",
                            "elementType": "labels.text.fill",
                            "stylers": [{
                                "color": "#757575"
                            }]
                        },
                        {
                            "featureType": "water",
                            "elementType": "geometry",
                            "stylers": [{
                                "color": "#000000"
                            }]
                        },
                        {
                            "featureType": "water",
                            "elementType": "labels.text.fill",
                            "stylers": [{
                                "color": "#3d3d3d"
                            }]
                        }
                    ]
                }
            }
        },
    }
</script>
<style lang="scss" scoped>
    .fade-enter-active,
    .fade-leave-active {
        transition: opacity .5s;
    }

    .fade-enter,
    .fade-leave-to

    /* .fade-leave-active до версии 2.1.8 */
        {
        opacity: 0;
    }

    .location_content {
        .location_content_title {
            text-transform: uppercase;
            font-size: 16px;
            line-height: 1.2307;
            font-weight: 400;
            color: #232a35;
            letter-spacing: 3px;
            margin-top: 26px;
        }

        .std__text {
            margin: 0px;
        }
    }

    .tab_list {
        .tab {
            cursor: pointer;
            color: black;
            text-decoration: none;
            margin-right: 12px;
            font-size: 18px;
            letter-spacing: 1px;
            vertical-align: top;
            text-transform: uppercase;
            transition: 1s;

            &.active {
                color: #FBBC04;
                transition: 1s;
            }
        }
    }

    .map-size {
        max-width: 100%;
        height: 500px;
    }



    ul {
        list-style-type: none;
        padding: 0px;
    }
</style>