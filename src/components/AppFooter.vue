<template>
    <footer>
        <section id="comics-footer">

            <div class="ms-container">
                <div class="nav-footer">

                    <div>
                        <h3>DC COMICS</h3>
                        <ul>
                            <li v-for="dcComics, e in dcComicsElements" :key="e">
                                <a :href="dcComics.link">
                                    {{dcComics.name}}
                                </a>
                            </li>
                        </ul>
                        <h3>SHOP</h3>
                        <ul>
                            <li v-for="shop, d in shopElements" :key="d">
                                <a :href="shop.link">
                                    {{shop.name}}
                                </a>
                            </li>
                        </ul>
                    </div>

                    <div>
                        <h3>DC</h3>
                        <ul>
                            <li v-for="dc, c in dcElements" :key="c">
                                <a :href="dc.link">
                                    {{dc.name}}
                                </a>
                            </li>
                        </ul>
                    </div>

                    <div>
                        <h3>SITES</h3>
                        <ul>
                            <li v-for="site, b in sitesElements" :key="b">
                                <a :href="site.link">
                                    {{site.name}}
                                </a>
                            </li>
                        </ul>
                    </div>

                </div>

                <div class="logo-footer">
                    <img :src="require(`@/assets/img/${logoFooter}`)" alt="logo dc">
                </div>

            </div>

        </section>

        <section id="social-footer">

            <div class="ms-container">

                <div class="btn-signup">
                    <a href="#">SIGN-UP NOW!</a>
                </div>

                <div class="socials">
                    <span>
                        FOLLOW US
                    </span>
                    <ul>

                        <li v-for="icon, a in iconsSocials" :key="a">
                            <a :href="icon.link">
                                <img :src="require(`@/assets/img/footer-${icon.pictureIcon}`)" :alt="icon.name">
                            </a>
                        </li>

                    </ul>

                </div>
            </div>
        </section>
    </footer>
</template>

<script>
export default {
    name: 'AppFooter',
    data() {
        return {
            logoFooter: 'dc-logo-bg.png',
            dcComicsElements: [

                {
                    link: '#',
                    name: 'Characters'
                },

                {
                    link: '#',
                    name: 'Comics'
                },

                {
                    link: '#',
                    name: 'Movies'
                },

                {
                    link: '#',
                    name: 'TV'
                },

                {
                    link: '#',
                    name: 'Games'
                },

                {
                    link: '#',
                    name: 'Videos'
                },
                {

                    link: '#',
                    name: 'News'
                }
            ],

            shopElements: [

                {
                    link: '#',
                    name: 'Shop DC'
                },

                {
                    link: '#',
                    name: 'Shop DC Collectibles'
                }
            ],

            dcElements: [

                {
                    link: '#',
                    name: 'Terms Of Use'
                },

                {
                    link: '#',
                    name: 'Privacy policy (New)'
                },

                {
                    link: '#',
                    name: 'Ad Choices'
                },

                {
                    link: '#',
                    name: 'Advertising'
                },

                {
                    link: '#',
                    name: 'Jobs'
                },

                {
                    link: '#',
                    name: 'Subscriptions'
                },

                {
                    link: '#',
                    name: 'Talent Workshops'
                },

                {
                    link: '#',
                    name: 'CPSC Certificates'
                },

                {
                    link: '#',
                    name: 'Ratings'
                },

                {
                    link: '#',
                    name: 'Shop Help'
                },

                {
                    link: '#',
                    name: 'Contact Us'
                },
            ],

            sitesElements: [
                {
                    link: '#',
                    name: 'DC'
                },

                {
                    link: '#',
                    name: 'MAD Magazine'
                },

                {
                    link: '#',
                    name: 'DC Kids'
                },

                {
                    link: '#',
                    name: 'DC Universe'
                },

                {

                    link: '#',
                    name: 'DC Power Visa'
                },

            ],

            iconsSocials: [

                {

                    link: '#',
                    name: 'facebook',
                    pictureIcon: 'facebook.png'
                },

                {
                    link: '#',
                    name: 'twitter',
                    pictureIcon: 'twitter.png'
                },

                {
                    link: '#',
                    name: 'youtube',
                    pictureIcon: 'youtube.png'
                },

                {
                    link: '#',
                    name: 'pinterest',
                    pictureIcon: 'pinterest.png'
                },

                {
                    link: '#',
                    name: 'periscope',
                    pictureIcon: 'periscope.png'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">

footer {
    display: flex;
    flex-direction: column;

    #comics-footer {
        height: 370px;
        background-image: url('../assets/img/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        overflow: hidden;

        .nav-footer {
            display: flex;
            width: 50%;
            padding: 20px 0;

            & div {
                margin-right: 30px;
            }

            h3 {
                color: white;
                margin: 20px 0 20px;
                font-size: 18px;
            }

            ul {
                list-style: none;

                li {
                    margin: 5px 0;

                    & a {
                        text-decoration: none;
                        color: #959595;
                        font-size: 14px;
                    }
                }
            }
        }

        .logo-footer {
            display: flex;
            justify-content: flex-end;
            width: 50%;
            position: relative;
            top: -100px;
            left: 0;
        }
    }

    #social-footer {
        width: 100%;
        background-color: #303030;
        padding: 20px 0;

        .btn-signup {
            display: flex;
            align-items: center;
            width: 50%;

            a {
                text-decoration: none;
                color: #fff;
                border: 2px solid #1068ba;
                padding: 10px 13px;
            }
        }
        .socials {
            display: flex;
            justify-content: flex-end;
            align-items: center;
            width: 50%;
            
            span {
                color: #0282f9;
                font-weight: 600;
                margin-right: 20px;
            }

            ul {
                list-style: none;
                
                & li {
                    display: inline-block;
                    margin: 0 10px;
                }
            }
        }
    }
}
</style>