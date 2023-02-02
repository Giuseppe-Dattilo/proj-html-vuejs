<script>
export default {
    name: 'BlogCard',
    props: {
        blog: Object
    }
}   
</script>

<template>
    <div class="card">
        <img role="button" :src="blog.thumb" :alt="blog.video">
        <h3 class="mb-0">{{ blog.video }}</h3>
        <div class="d-flex">
            <img id="icon" src="../../assets/img/55281.png" alt="calendar">
            <h5> {{ blog.date }}</h5>
        </div>

        <p> {{ blog.description }}</p>
    </div>
</template>

<style scoped lang="scss">
@use '../../assets/scss/partials/variables' as *;

.card {
    min-height: 450px;
    padding: 10px;
    background-color: black;


    img {
        display: block;

        &:hover {
            transform: scale(1.1);
        }
    }

    #icon {
        margin: 13px 5px;
        width: 10px;
        height: 10px;
        filter: invert(50%) sepia(50%) saturate(5) hue-rotate(300deg);
    }

    h3 {
        margin-top: 15px;
        font-size: 20px;
        font-weight: bolder;
        text-align: left;
    }

    h5 {
        color: $red;
        font-size: 13px;
        text-align: left;
        margin-top: 10px;
    }

    p {
        color: grey;
        font-size: 13px;
        margin-top: 10px;
        text-align: left;
    }
}
</style>