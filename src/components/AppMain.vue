<script>
import VideosCard from './videos/VideosCard.vue';
export default {
    nome: 'AppMain',
    components: { VideosCard },
    props: {
        videos: Array
    },
}


</script>

<template>
    <main>
        <section id="jazz">
            <div class="container text-center">
                <h6>WHO WE ARE</h6>
                <h2>SENSE THE JAZZ</h2>
                <div class="container card-container">
                    <videos-card v-for="video in videos" :key="video.thumb" :video="video"></videos-card>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
#jazz {
    background-color: black;
    color: white;
    padding: 4rem 1rem;
    min-height: 150px;

    h6 {
        font-size: 15px;
        color: #f2870c;
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
</style>