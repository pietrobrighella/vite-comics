<template>
    <main>
        <section class="container">
            <div class="current-series">Current Series</div>
            <div class="card-group">
                <CardComponent />
            </div>
        </section>
    </main>
</template>

<script>
import CardComponent from './CardComponent.vue';

    export default {
    name: "MainComponent",
    components: { CardComponent }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

main {
    background-color: $dark;
}
.card-group {
    color: $white;
    display: flex;
    justify-content: space-between;
    flex-flow: row wrap;
    text-transform: uppercase;
    padding: 2rem 0;
    gap: 5px;
}
.current-series {
    width: 160px;
    height: 40px;
    background-color: $blue;
    text-align: center;
    color: $white;
    text-transform: uppercase;
    line-height: 40px;
    font-size: 1rem;
    font-weight: 800;
    margin-top: -35px;
}
</style>