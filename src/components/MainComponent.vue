<template>
    <h2> --&gt; Content goes here &lt;-- </h2>
</template>

<script>
    export default {
        name: 'MainComponent'
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

h2 {
    background-color: $dark;
    color: $white;
    text-align: center;
    min-height: 120px;
    line-height: 120px;
}
</style>