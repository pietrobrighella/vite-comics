<template>
    <section>
        <div class="container">
            <button>Sign-Up now!</button>
            <div>
                <h4>Follow us</h4>
                <ul>
                    <li v-for="(link, index) in socialLink" :key="index">
                        <a href="#">
                            <img :src="link.iconUrl" :alt="link.name">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'SubFooterComponent',
        data() {
            return {
                socialLink: [
                    {
                        name: 'Facebook',
                        iconUrl: '/public/assets/img/footer-facebook.png',
                    },
                    {
                        name: 'Twitter',
                        iconUrl: '/public/assets/img/footer-twitter.png',
                    },
                    {
                        name: 'YouTube',
                        iconUrl: '/public/assets/img/footer-youtube.png',
                    },
                    {
                        name: 'Pinterest',
                        iconUrl: '/public/assets/img/footer-pinterest.png',
                    },
                    {
                        name: 'Periscope',
                        iconUrl: '/public/assets/img/footer-periscope.png',
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

section {
    background-color: $lightdark;
    height: 80px;
    div.container {
        @include dflex;
        justify-content: space-between;
        height: 100%;

        button {
            padding: 0.6rem 1rem;
            text-transform: uppercase;
            background: transparent;
            border: 1px solid $blue;
            color: $white;
            font-weight: 400;
            cursor: pointer;

            &:hover {
                background-color: $blue;
                color: $dark;
                font-weight: 800;
            }
        }

        div {
            @include dflex;
            gap: 10px;

            ul {
                @include dflex;
                gap: 10px;

                li a:hover {
                    filter: brightness(3);
                }
            }

            h4 {
                color: $blue;
                text-transform: uppercase;
                font-size: 1rem;
                padding-right: 1rem;
            }
        }
    }
}
</style>