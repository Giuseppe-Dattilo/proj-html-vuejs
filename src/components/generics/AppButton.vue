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
@use '../../assets/scss/partials/variables' as *;

button {
    padding: 7px 40px;
    background-color: transparent;
    border: 1px solid $red;
    color: white;
    cursor: pointer;

    &:hover {
        background-color: $red;
    }
}
</style>