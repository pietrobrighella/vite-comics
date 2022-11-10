<template>
    <header>
        <div class="container">
            <a href="#">
                <img src="../assets/img/dc-logo.png" alt="DC Comics logo">
            </a>
            <nav>
                <ul>
                    <li v-for="(link, index) in headerLinks" :key="index">
                        <a :href="link.url" :class="{'active': link.current}">{{link.text}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data() {
            return {
                headerLinks: [
                {
                    text: "Characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "Tv",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                },
            ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

header {
    background-color: $white;

        div {
        text-align: center;
        height: 80px;
        justify-content: space-between;
        @include dflex;

        a {
            line-height: 0;
            & img {
                height: 60px;
            }
        }

        nav ul {
            list-style: none;
            height: 100%;
            @include dflex;

            li a {
                display: inline-block;
                padding: .6rem;
                font-size: .8rem;
                text-decoration: none;
                text-transform: uppercase;
                font-weight: 600;
                color: $dark;
                position: relative;

                &.active,
                &:hover {
                    color: $blue;

                    &::after {
                    content:'';
                        margin-top: 30px;
                        width: 100%;
                        height: 4px;
                        background-color: $blue;
                        position: absolute;
                        bottom: -30px;
                        left: 0;
                    }
                }
            }
        }
    }
}

</style>