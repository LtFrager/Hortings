<template>
    <div>
        <my-map :data="locationData" />

        <!-- <h2 data-aos="zoom-in" data-aos-duration="1000" data-aos-delay="300"
            class="std__title text__black text-xs-center">
            <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">контакти </span>
            Секцiй
        </h2> -->

        <!-- <sections :data="SectionsData" /> -->
    </div>

</template>
<script>
    import PromoCards from '@/components/PromoCards'
    import TitlePromo from '@/components/TitlePromo'
    import ListBlock from '@/components/ListBlock'
    import TextBlock from '@/components/TextBlock'
    import MyMap from '@/components/contacts/MyMap'
    import Sections from '@/components/contacts/Sections'
    export default {
        components: {
            PromoCards,
            TitlePromo,
            ListBlock,
            TextBlock,
            MyMap,
            Sections
        },
        data() {
            return {
                  locationData: [{
                        active: 1,
                        title: 'Київ',
                        text: '',
                        contactsData: [{
                                contacsTitle: 'Адресса',
                                contactsContent: [
                                    '04205, Київ, пр-т Оболонський, 10-53.',
                                ]
                            },
                            {
                                contacsTitle: 'Телефон',
                                contactsContent: [
                                    '+38-068-978-48-85',
                                    '+38-073-155-39-07'
                                ]
                            },
                            {
                                contacsTitle: 'E-mail',
                                contactsContent: [
                                    'horting.fencing@gmail.com',
                                ]
                            }
                        ],
                        position: {
                            lat: 50.4547,
                            lng: 30.5238
                        }
                    },
                    // {
                    //     active: 2,
                    //     title: 'Днепропетровск',
                    //     text: 'Place 2 active  Plase for text',
                    //     contactsData: [{
                    //             contacsTitle: 'Adress',
                    //             contactsContent: [
                    //                 '2 4096 N Highland St, Arlington VA 32101, USA',
                    //             ]
                    //         },
                    //         {
                    //             contacsTitle: 'Phone',
                    //             contactsContent: [
                    //                 '800 1234 56 78',
                    //                 '800 1234 56 78'
                    //             ]
                    //         },
                    //         {
                    //             contacsTitle: 'mail',
                    //             contactsContent: [
                    //                 'school@company.com',
                    //             ]
                    //         }
                    //     ],
                    //     position: {
                    //         lat: 50.4547,
                    //         lng: 10.123238
                    //     }
                    // },
                ],

                SectionsData: [
                    {
                        cityName: "City1",
                        citySections: [{
                                sectionName: "Section 1",
                                sectionsDescr: [{
                                    sectionPhone: ["phone1", "phone2"],
                                    sectionEmail: ["mail1", "mail2"],
                                    sectionAdress: ["link", "adress"],
                                }]
                            },
                            {
                                sectionName: "Section 1",
                                sectionsDescr: [{
                                    sectionPhone: ["phone1", "phone2"],
                                    sectionEmail: ["mail1", "mail2"],
                                    sectionAdress: ["link", "adress"],
                                }]
                            }
                        ]
                    },

                    {
                        cityName: "City2",
                        citySections: [{
                            sectionName: "Section 1",
                            sectionsDescr: [{
                                sectionPhone: ["phone1", "phone2"],
                                sectionEmail: ["mail1", "mail2"],
                                sectionAdress: ["link", "adress"],
                            }]
                        }]
                    }
                ]
            }
        }
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
            color: #9f9f9f;
            font-size: 18px;
            line-height: 30px;
            font-weight: 300;
            margin-bottom: 6px;
            letter-spacing: 1px;
            line-height: 1;
            text-transform: none;
        }
    }
</style>