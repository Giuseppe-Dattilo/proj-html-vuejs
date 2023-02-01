<script>
export default {
    name: 'SectionGallery',
    props: {
        picture: Object
    }
}
</script>

<template>
    <div>
        <ul class="mb-0 p-0">
            <li class="d-flex">
                <a href="#"><img role="button" :src="picture.thumb" :alt="picture.thumb"></a>
            </li>
        </ul>
    </div>



</template>

<style scoped lang="scss">
img {
    width: 200px;
}
</style>