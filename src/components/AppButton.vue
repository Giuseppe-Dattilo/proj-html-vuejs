<script>
export default {
    name: 'AppButton',
    props: {
        buttonLabel: String
    },
    emits: ['button-clicked'],
}
</script>

<template>
    <button @click="$emit('button-clicked')">{{ buttonLabel }}</button>
</template>

<style lang="scss" scoped>
button {
    padding: 7px 40px;
    background-color: transparent;
    border: 1px solid #f2870c;
    color: white;
    cursor: pointer;

    &:hover {
        background-color: #f2870c;
    }
}
</style>