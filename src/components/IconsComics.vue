<template>

    <section id="icons-main">

        <div class="ms-container">
            <nav>
                <ul>
                    <li v-for="comicsEl, j in comicsElements" :key="j">
                        <a :href="comicsEl.link">
                            <img :src="require(`@/assets/img/${comicsEl.picture}`)" :alt="comicsEl.text">
                            <span>{{comicsEl.text}}</span>
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </section>

</template>

<script>

export default {
  name: 'IconsComics',
  data() {

      return {

          comicsElements: [

            {
                text: 'DIGITAL COMICS',
                link: '#',
                picture: 'buy-comics-digital-comics.png'
            },

            {
                text: 'DC MERCHANDISE',
                link: '#',
                picture: 'buy-comics-merchandise.png'
            },

            {
                text: 'SUBSCRIPTION',
                link: '#',
                picture: 'buy-comics-subscriptions.png'
            },

            {
                text: 'COMICS SHOP LOCATOR',
                link: '#',
                picture: 'buy-comics-shop-locator.png'
            },

            {
                text: 'DC POWER VISA',
                link: '#',
                picture: 'buy-dc-power-visa.svg'
            }

          ]
        }
    }   
}
</script>

<style scoped lang="scss">

    #icons-main {
        padding: 50px 0;
        width: 100%;
        background-color: #0282f9;

        nav {

            ul {
                display: flex;
                list-style: none;

                li {
                    margin: 0 29px;

                    a {
                        display: flex;
                        align-items: center;
                        text-decoration: none;
                        color: #fff;
                        font-size: 14px;

                        img {
                            width: 55px;
                            height: 65px;
                        }

                        span {
                            margin-left: 15px;
                        }
                    }
                }
                
                li:nth-child(4) {
                    img {
                        width: 45px;
                    }
                }
            }
        }
    }
</style>