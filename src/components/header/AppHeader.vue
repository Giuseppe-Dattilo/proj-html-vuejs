<script>
import SectionVideo from './SectionVideo.vue'
import SectionJazz from './SectionJazz.vue';
export default {
    nome: 'Appheader',
    components: { SectionVideo, SectionJazz },
    data() {
        return {
            links: [
                {
                    text: 'home',
                    url: '#',
                    active: true,
                },
                {
                    text: 'blog',
                    url: '#',
                    active: false,
                },
                {
                    text: 'events',
                    url: '#',
                    active: false,
                },
                {
                    text: 'gallery',
                    url: '#',
                    active: false,
                },
                {
                    text: 'about us',
                    url: '#',
                    active: false,
                },
                {
                    text: 'contact us',
                    url: '#',
                    active: false,
                },
                {
                    text: 'shop',
                    url: '#',
                    active: false,
                },
            ]
        }
    }
};
</script>

<template>
    <header>

        <nav>
            <!-- left nav -->
            <figure class="mb-0">
                <a href="#"><img src="../../assets/img/Logo.png" alt="lyricmusic"></a>
            </figure>

            <!-- right nav -->
            <ul>
                <li v-for="link in links" :key="link.text">
                    <a :href="link.url" v-text="link.text" :class="{ 'active': link.active }"></a>
                </li>
            </ul>
        </nav>

    </header>
    <section-video collection="video" title="INSTRUMENTAL ROCK" mainTitle="MUSIC IN THIS VIDEO"></section-video>
    <section-jazz collection="jazz" title="WHO WE ARE" mainTitle="SENSE THE JAZZ"></section-jazz>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/mixins' as *;

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0;
    height: 80px;
    background-color: black;

    img {
        height: 30px;
        margin-left: 30px
    }
}

ul {
    @include center_flex;
    margin: 30px;
    padding: 0;

    li {
        list-style-type: none;

        a {
            padding: 20px;
            color: white;
            font-size: 15px;
            text-transform: uppercase;

            &.active {
                color: #f2870c;
            }

            &:hover {
                background-color: #f2870c;
                color: white;
            }

        }
    }
}
</style>