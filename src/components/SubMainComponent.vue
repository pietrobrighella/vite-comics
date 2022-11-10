<template>
    <section>
        <div class="container container-main-content">
            <div class="main-content" v-for="(content, index) in subMainContent" :key="index">
                <div class="image"><img :src="content.image" :alt="content.name"></div>
                <h4>{{content.name}}</h4>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'SubMainComponent',
        data() {
            return {
                subMainContent: [
                    {
                        name: 'Digital comics',
                        image: '/assets/img/buy-comics-digital-comics.png'
                    },
                    {
                        name: 'DC Merchandise',
                        image: '/assets/img/buy-comics-merchandise.png'
                    },
                    {
                        name: 'Subscription',
                        image: '/assets/img/buy-comics-subscriptions.png'
                    },
                    {
                        name: 'Comic shop locator',
                        image: '/assets/img/buy-comics-shop-locator.png'
                    },
                    {
                        name: 'DC Power VISA',
                        image: '/assets/img/buy-dc-power-visa.svg'
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

section {
    background-color: $blue;

    .container-main-content {
        display: flex;
        flex-flow: row nowrap;
        justify-content: space-around;
    }
    .main-content {
        display: flex;
        flex-flow: row nowrap;
        align-items: center;
        color: $white;
        text-transform: uppercase;

        h4 {
            font-size: .8rem;
            font-weight: 400;
        }
        .image {
            width: 2rem;
            margin: .8rem;
            text-align: center;

            & img {
                max-height: 2.3rem;
            }
        }
    }
}

</style>