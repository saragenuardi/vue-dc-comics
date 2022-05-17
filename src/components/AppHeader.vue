<template>
    <header>
        <div>
            <img src="../assets/img/dc-logo.png"/>
        </div>
        <nav>
            <ul>
                <li v-for="el, i in AppHeader" :key:"i">
                    <a :href="el.link" :class="el.selected ? 'active' : ''">
                        {{ el.text}}
                    </a>

                </li>
            </ul>
        </nav>
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

</style>
