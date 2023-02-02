<script>
import SectionGallery from './SectionGallery.vue';
import BlogCard from './BlogCard.vue';
import VideosCard from './VideosCard.vue';
import NewVideo from './NewVideo.vue';
import NewAlbum from './NewAlbum.vue';
import Counter from './Counter.vue';
export default {
    nome: 'AppMain',
    components: { VideosCard, NewVideo, NewAlbum, Counter, BlogCard, SectionGallery },
    props: {
        videos: Array,
        blogs: Array,
        pictures: Array
    },
}


</script>

<template>
    <new-video collection="new-video" mainTitle="NEW MUSIC VIDEO"></new-video>
    <section class="prod-card">
        <div class="container text-center">
            <h6>WHO WE ARE</h6>
            <h2>SENSE THE JAZZ</h2>
            <div class="container card-container">
                <videos-card v-for="video in videos" :key="video.thumb" :video="video"></videos-card>
            </div>
        </div>
    </section>
    <new-album collection="new-album" title="INSTRUMENTAL ROCK" mainTitle="ALBUM OUT NOW"></new-album>
    <counter collection="counter"></counter>
    <section class="prod-card">
        <div class="container text-center">
            <h6>MUSIC BLOG</h6>
            <h2>BEST MUSIC BLOG</h2>
            <div class="container card-container">
                <blog-card v-for="blog in blogs" :key="blog.thumb" :blog="blog"></blog-card>
            </div>
        </div>
    </section>
    <section>
        <div>
            <div class="gallery">
                <section-gallery v-for="picture in pictures" :key="picture.id" :picture="picture"></section-gallery>
            </div>
        </div>
    </section>

</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/variables' as *;

.prod-card {
    background-color: black;
    color: white;
    padding: 4rem 1rem;
    min-height: 150px;

    h6 {
        font-size: 15px;
        color: $red;
    }

    h2 {
        font-size: 50px;
        font-weight: bold;
    }

    .card-container {
        display: flex;
        flex-wrap: wrap;
        margin-top: 2rem;

        .card {
            flex-basis: calc(100% / 3);
        }
    }
}

.gallery {
    display: flex;
}
</style>