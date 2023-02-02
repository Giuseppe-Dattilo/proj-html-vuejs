<script>
export default {
    name: 'SectionGallery',
    props: {
        picture: Object
    }
}
</script>

<template>
    <div class="gallery">
        <ul class="mb-0 p-0">
            <li class="d-flex">
                <a href="#"><img class="img-fluid" role="button" :src="picture.thumb" :alt="picture.thumb"></a>
            </li>
        </ul>
    </div>



</template>

<style scoped lang="scss">
.gallery {
    width: 100%;
    background-color: black;

    img {
        width: 200px;

        &:hover {
            transform: scale(1.1);
        }

    }
}
</style>