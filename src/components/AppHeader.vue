<template>
    <header>
        <div class="ms-container">
            <section id="logo-header">
                <img src="../assets/img/dc-logo.png" alt="dc logo">
            </section>
            <nav>
                <ul>
                    <li v-for="el, index in NavComics" :key="index">
                        <a :href="el.link" :class="el.selected ? 'active' : '' ">
                            {{el.text}}
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
export default {
    name: "AppHeader",
    data: function() {
        return {
            NavComics: [
                {
                    text: 'CHARACTERS',
                    link: '#',
                    selected: false
                },

                {
                    text: 'COMICS',
                    link: '#',
                    selected: true
                },

                {
                    text: 'MOVIES',
                    link: '#',
                    selected: false
                },

                {
                    text: 'TV',
                    link: '#',
                    selected: false
                },

                {
                    text: 'GAMES',
                    link: '#',
                    selected: false
                },

                {
                    text: 'COLLECTIBLES',
                    link: '#',
                    selected: false
                },

                {
                    text: 'VIDEOS',
                    link: '#',
                    selected: false
                },

                {
                    text: 'FANS',
                    link: '#',
                    selected: false
                },

                {
                    text: 'NEWS',
                    link: '#',
                    selected: false
                },

                {
                    text: 'SHOP',
                    link: '#',
                    selected: false
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
   header {
    width: 100%;
    
    #logo-header {
        display: flex;
        width: 30%;
        padding: 20px 0;

        img {
            height: 85px;
            width: 85px;
        }
    }
    nav {
        display: flex;
        justify-content: flex-end;
        align-items: center;
        width: 70%;

        ul {
            list-style: none;

            li {
                display: inline-block;
                margin: 0 10px;

                a {
                    text-decoration: none;
                    color: #4d5056;
                    font-size: 15px;
                    font-weight: 600;

                    &.active {
                        color: #2c89f9;
                        border-bottom: 7px solid #2c89f9;
                        padding-bottom: 47px;
                    }
                }
            }
        }
    }
   }
</style>
