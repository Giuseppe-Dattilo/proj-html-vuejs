<script>
export default {
    name: 'Counter',
    props: {
        collection: String,
    },
}
</script>

<template>
    <section :id="collection">
        <div class="counter">
            <div class="result">
                <img src="../../assets/img/image (13).svg" alt="">
                <h2>163</h2>
                <h5>CONCERTS</h5>
            </div>
            <div class="result">
                <img src="../../assets/img/image (14).svg" alt="">
                <h2>145</h2>
                <h5>HAPPY CLIENTS</h5>
            </div>
            <div class="result">
                <img src="../../assets/img/image (15).svg" alt="">
                <h2>72</h2>
                <h5>MUSIC AWARDS</h5>
            </div>
            <div class="result">
                <img src="../../assets/img/image (16).svg" alt="">
                <h2>182</h2>
                <h5>TOTAL SONGS</h5>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../../assets/scss/partials/mixins' as *;

.counter {
    @include center_flex;
    background-image: url(../../assets/img/counter_parallax.jpg);
    min-height: 350px;
    background-size: cover;

    .result {
        display: flex;
        flex-direction: column;
        align-items: center;
        color: white;
        margin: 0 80px;

        img {
            width: 40px;
            margin-bottom: 20px;
            filter: invert(100%);

            // filter: invert(0.5) sepia(1) saturate(5) hue-rotate(10deg);
        }

        h2 {
            font-size: 50px;
            font-weight: bolder;
        }

        h5 {
            font-weight: bolder;
        }
    }


}
</style>