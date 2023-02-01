<script>
export default {
    name: 'VideosCard',
    props: {
        video: Object
    }
}   
</script>

<template>
    <div class="card">
        <img role="button" :src="video.thumb" :alt="video.videos">
        <h3 class="mb-0">{{ video.videos }}</h3>
        <div class="sub-icon d-flex align-items-center justify-content-center">
            <h6> {{ video.sub }}</h6>
            <ul>
                <!-- icon -->
                <li class="d-flex">
                    <a href="#"><img src="../../assets/img/image (20).svg" alt="spotify"></a>
                    <a href="#"><img src="../../assets/img/image (20).svg" alt="youtube"></a>
                    <a href="#"><img src="../../assets/img/image (16).svg" alt="note"></a>
                    <a href="#"><img src="../../assets/img/image (20).svg" alt="cloud"></a>
                    <a href="#"><img src="../../assets/img/image (20).svg" alt="flag"></a>
                </li>
            </ul>

        </div>
    </div>
</template>

<style scoped lang="scss">
.card {
    padding: 10px;
    background-color: black;

    ul {
        padding: 0;
        margin-left: 5px;

        li {
            list-style-type: none;
            margin-top: 8px;

            a {
                padding: 0 5px;

                img {
                    width: 10px;
                    filter: invert(100%);

                    &:hover {
                        filter: invert(0.5) sepia(1) saturate(5) hue-rotate(10deg);
                    }

                }
            }

        }
    }



    img {
        display: block;

        &:hover {
            transform: scale(1.1);
        }
    }

    h3 {
        margin-top: 15px;
        font-size: 20px;
        font-weight: bolder;
        text-transform: uppercase;
    }

    h6 {
        color: grey;
    }
}
</style>