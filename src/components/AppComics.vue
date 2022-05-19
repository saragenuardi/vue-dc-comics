<template>
    <div class="comics">
        <!-- Componente jumbotron Comics -->
        <JumbotronComics/>

        <section id="content-main">

            <div class="ms-container">
                <div class="title-comics">
                    <h2>CURRENT SERIES</h2>
                </div>
                
                <div class="cards-comics">
                    <!-- Componente cards Comics -->
                    <CardsComics v-for="card, i in cards" :key="i"
                    :details="card"/>
                </div>

                <div class="more-cards">
                    <a href="#">LOAD MORE</a>
                </div>

            </div>
        </section>

        <!-- Componente Icons Comics -->
        <IconsComics/>

    </div>
</template>

<script>
import IconsComics from './IconsComics.vue'
import JumbotronComics from './JumbotronComics.vue'
import CardsComics from './CardsComics.vue'

export default {

    name: 'AppComics',

    components: {
        IconsComics,
        JumbotronComics,
        CardsComics
    },

    data() {

        return {
            cards: [

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },

                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">

$color_text: #fff;
$primary_color: #0282f9;

div.comics {

    display: flex;
    flex-direction: column;

    .ms-container {
        
        flex-direction: column;
    }
    #content-main {

        width: 100%;
        background-color: #1c1c1c;
        padding: 20px 0;

        .title-comics {
            width: max-content;
            color: $color_text;
            font-size: 16px;
            padding: 16px 20px;
            background-color: $primary_color;
            position: relative;
            top: -50px;
            left: 0;
        }

        .cards-comics {
            display: flex;
            flex-wrap: wrap;
        }

        .more-cards {
            display: flex;
            justify-content: center;
            align-items: center;
            
            a {
                text-decoration: none;
                color: $color_text;
                padding: 15px 65px;
                font-weight: 600;
                font-size: 14px;
                background-color: $primary_color;
            }
        }
    }
}
</style>