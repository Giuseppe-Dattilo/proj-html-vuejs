<script>
import AppButton from '../generics/AppButton.vue';
export default {
    name: 'SectionJazz',
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
        <div class="jazz">
            <h6>{{ title }}</h6>
            <h1>{{ mainTitle }}</h1>
            <p class="text-center">the story of jazz and blues society is the story of determination, passion,
                idealism,community, and of
                course, music. founded in 1985 and incorporated in 1986, as a community based, not-for-profit,charitable
                artsorganization located in vancouver british columbia tue csociety, from the very beginning, has worked
                diligently to establish vancouver as a centre for the creation and exchange of sound and ideas between
                the local, national and international music communities. </p>
            <app-button :buttonLabel="'READ MORE'"></app-button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/mixins' as *;
@use '../../assets/scss/partials/variables' as *;

.jazz {
    @include center_flex;
    flex-direction: column;
    background-color: black;
    min-height: 650px;
    background-size: cover;

    h1 {
        color: white;
        font-weight: bolder;
        font-size: 50px;
        margin-bottom: 20px
    }

    h6 {
        color: $red;
        margin-bottom: 20px;
        font-size: 15px;
    }

    p {
        text-transform: capitalize;
        color: white;
        padding: 0 300px;
        margin-bottom: 50px;
    }

}
</style>