<script>
import AppButton from '../AppButton.vue';
export default {
    name: 'NewAlbum',
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
        <div class="new-album">
            <h6>{{ title }}</h6>
            <h1>{{ mainTitle }}</h1>
            <div>
                <app-button :buttonLabel="'READ MORE'"></app-button>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
.new-album {
    display: flex;
    justify-content: center;
    flex-direction: column;
    background-image: url(../../assets/img/cms_parallax.jpg);
    min-height: 650px;
    padding-left: 200px;
    background-size: cover;

    h1 {
        color: white;
        font-weight: bolder;
        font-size: 90px;
        margin-bottom: 20px
    }

    h6 {
        color: #f2870c;
        font-size: 20px;
        font-weight: bolder;
        text-align: left;
    }

}
</style>