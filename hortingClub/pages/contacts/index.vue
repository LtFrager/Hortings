<template>
    <div>
        <my-map :data="locationData" />

         <h2 data-aos="zoom-in" data-aos-duration="1000" data-aos-delay="300"
            class="std__title text__black text-xs-center">
            <span data-aos="slide-up" data-aos-delay="800" data-aos-duration="1000" class="subtitle">контакти </span>
            Секцiй
        </h2>

        <sections :data="SectionsData" /> 
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
                                contacsTitle: 'Адреса',
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
                        cityName: "Київ",
                        citySections: [{
                                sectionName: "Клуб ХОРТИНГ ФЕХТУВАННЯ у 75-й гімназії міста Києва.",
                                // Розклад занять: Понеділок, середа, п'ятниця з 15.30 до 17.30
                                sectionsDescr: [{
                                    sectionPhone: ["+380688775404", "+380673454191"],
                                    // sectionEmail: ["mail1", "mail2"],
                                    sectionAdress: ["https://www.google.com/maps/search/%D0%91%D1%83%D1%82%D0%B8%D1%88%D1%96%D0%B2+%D0%BF%D1%80%D0%BE%D0%B2%D1%83%D0%BB%D0%BE%D0%BA,+11,+%D0%9A%D0%B8%D1%97%D0%B2,+02000/@50.4395612,30.5434879,17z/data=!3m1!4b1", "Бутишів провулок, 11, Київ, 02000"],
                                }]
                            },

                            {
                                sectionName: "Клуб ХОРТИНГ ФЕХТУВАННЯ (Троєщина)",
                                sectionsDescr: [{
                                    sectionPhone: ["+380 67 238 38 43"],
                                    // sectionEmail: ["mail1", "mail2"],
                                    sectionAdress: ["https://www.google.com/maps?rlz=1C1ASUM_enUA873UA873&biw=1858&bih=1009&sxsrf=ALeKk03MNlDZBInrRNED5EAn9YbEQGZ6sg:1599908169072&q=%D0%9A%D0%B8%D1%97%D0%B2,+%D0%94%D0%B5%D1%81%D0%BD%D1%8F%D0%BD%D1%81%D1%8C%D0%BA%D0%B8%D0%B9+%D1%80%D0%B0%D0%B9%D0%BE%D0%BD,+%D0%B2%D1%83%D0%BB.+%D0%91%D1%83%D0%B4%D0%B8%D1%89%D0%B0%D0%BD%D1%81%D1%8C%D0%BA%D0%B0+3&gs_lcp=CgZwc3ktYWIQAzICCCYyAggmUMCHAVjAhwFgl4oBaABwAHgAgAFjiAFjkgEBMZgBAKABAqABAaoBB2d3cy13aXrAAQE&uact=5&um=1&ie=UTF-8&sa=X&ved=2ahUKEwiDjrHLuuPrAhVmpYsKHcDKDAIQ_AUoAXoECA8QAw", "Київ, Деснянський район, вул. Будищанська 3"],
                                }]
                            },
                              {
                                sectionName: "CLUB GLADIATORIA - фехтувальний клуб",
                                sectionsDescr: [{
                                    sectionPhone: ["+380 93 573 53 00"],
                                    // sectionEmail: ["mail1", "mail2"],
                                    sectionAdress: ["https://www.google.com/maps/place/%D0%A1%D0%BF%D0%B5%D1%86%D1%96%D0%B0%D0%BB%D1%96%D0%B7%D0%BE%D0%B2%D0%B0%D0%BD%D0%B0+%D1%88%D0%BA%D0%BE%D0%BB%D0%B0+%D0%86-%D0%86%D0%86+%D1%81%D1%82%D1%83%D0%BF%D0%B5%D0%BD%D1%96%D0%B2+-+%D0%BB%D1%96%D1%86%D0%B5%D0%B9+%E2%84%96157/@50.5038635,30.5034183,17z/data=!4m8!1m2!2m1!1z0JrQuNGX0LIsINCe0LHQvtC70L7QvdGB0YzQutC40Lkg0YDQsNC50L7QvSwg0L3QsCDRgtC10YDQuNGC0L7RgNGW0Zcg0LvRltGG0LXRjiDihJYxNTc!3m4!1s0x40d4d20fefba527f:0x16703e8fecde3cc1!8m2!3d50.5041799!4d30.5026103", "Київ, Оболонський район, на території ліцею №157"],
                                }]
                            },
                                {
                                sectionName: "Клуб фехтування у Шевченковскому районі (м. Лук'янівська)",
                                sectionsDescr: [{
                                    sectionPhone: ["067 238 4000"],
                                    // sectionEmail: ["mail1", "mail2"],
                                    sectionAdress: ["https://www.google.com/maps/place/%D1%83%D0%BB.+%D0%9F%D0%BE%D0%BB%D0%BE%D0%B2%D0%B5%D1%86%D0%BA%D0%B0%D1%8F,+49,+%D0%9A%D0%B8%D0%B5%D0%B2,+02000/data=!4m2!3m1!1s0x40d4ce79e5331bff:0xa81ffbf7899a0165?sa=X&ved=2ahUKEwjOr_Ktu-PrAhXOlYsKHaPPDasQ8gEwAHoECAsQAQ", "Київ, Шевченковскій район, вул. Половецька, 49"],
                                }]
                            }
                        ]
                    },

            
                    // {
                    //     cityName: "City2",
                    //     citySections: [{
                    //         sectionName: "Section 1",
                    //         sectionsDescr: [{
                    //             sectionPhone: ["phone1", "phone2"],
                    //             sectionEmail: ["mail1", "mail2"],
                    //             sectionAdress: ["link", "adress"],
                    //         }]
                    //     }]
                    // }
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