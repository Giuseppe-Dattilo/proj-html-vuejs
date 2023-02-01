<script>
import AppButton from '../AppButton.vue';
export default {
    name: 'SectionVideo',
    components: { AppButton },
    props: {
        title: String,
        mainTitle: String,
        collection: String,
    },
}
</script>

<template>
    <section :id="collection">
        <div class="video">
            <h6>{{ title }}</h6>
            <h1>{{ mainTitle }}</h1>
            <app-button :buttonLabel="'READ MORE'"></app-button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/mixins' as *;

.video {
    @include center_flex;
    flex-direction: column;
    background-image: url(../../assets/img/jumbotron.png);
    min-height: 650px;
    background-size: cover;

    h1 {
        color: white;
        font-weight: bolder;
        font-size: 80px;
        margin-bottom: 20px
    }

    h6 {
        color: #f2870c;
        margin-bottom: 20px;
        font-size: 20px;
    }

}
</style>