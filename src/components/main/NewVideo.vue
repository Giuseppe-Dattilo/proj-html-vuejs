<script>
export default {
    name: 'NewVideo',
    props: {
        mainTitle: String,
        collection: String,
    },
}
</script>

<template>
    <section :id="collection">
        <div class="new-video">
            <img src="../../assets/img/red-play-button-icon-icons-15.png" alt="play">
            <h1>{{ mainTitle }}</h1>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/mixins' as *;

.new-video {
    @include center_flex;
    flex-direction: column;
    background-image: url(../../assets/img/Video.jpg);
    min-height: 500px;
    background-size: cover;

    img {
        width: 70px;
        margin-bottom: 20px;
        cursor: pointer;

        filter: invert(0.5) sepia(1) saturate(5) hue-rotate(10deg);
    }

    h1 {
        color: white;
        font-weight: bolder;
        font-size: 50px;
        margin-bottom: 20px
    }
}
</style>