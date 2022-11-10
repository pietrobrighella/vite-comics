<template>
    <footer>
        <div class="container">
            <div>
                <div class="menu-block-1">
                    <h4>{{firstMenu.title}}</h4>
                    <ul>
                        <li v-for="(link, index) in firstMenu.listMenu" :key="index">
                            <a href="#">{{link.term}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h4>{{secondMenu.title}}</h4>
                    <ul>
                        <li v-for="(link, index) in secondMenu.listMenu" :key="index">
                            <a href="#">{{link.term}}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="menu-block-2">
                <div>
                    <h4>{{thirdMenu.title}}</h4>
                    <ul>
                        <li v-for="(link, index) in thirdMenu.listMenu" :key="index">
                            <a href="#">{{link.term}}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h4>{{fourthMenu.title}}</h4>
                    <ul>
                        <li v-for="(link, index) in fourthMenu.listMenu" :key="index">
                            <a href="#">{{link.term}}</a>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="img-overflow">
                <div>
                    <img class="img-footer" src="../assets/img/dc-logo-bg.png" alt="DC Comics logo">
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
    export default {
        name: 'FooterComponent',
        data() {
            return {
                firstMenu: {
                    title: 'Dc Comics',
                    listMenu: [
                        {
                            term: 'Characters',
                            link: '#'
                        },
                        {
                            term: 'Comics',
                            link: '#'
                        },
                        {
                            term: 'Movies',
                            link: '#'
                        },
                        {
                            term: 'TV',
                            link: '#'
                        },
                        {
                            term: 'Games',
                            link: '#'
                        },
                        {
                            term: 'Videos',
                            link: '#'
                        },
                        {
                            term: 'News',
                            link: '#'
                        }
                    ]
                },
                secondMenu: {
                    title: 'Shop',
                    listMenu: [
                        {
                            term: 'Shop DC',
                            link: '#'
                        },
                        {
                            term: 'Shop DC Collectibles',
                            link: '#'
                        }
                    ]
                },
                thirdMenu: {
                    title: 'DC',
                    listMenu: [
                        {
                            term: 'Term Of Use',
                            link: '#'
                        },
                        {
                            term: 'Privacy policy (New)',
                            link: '#'
                        },
                        {
                            term: 'Ad Choices',
                            link: '#'
                        },
                        {
                            term: 'Advertising',
                            link: '#'
                        },
                        {
                            term: 'Jobs',
                            link: '#'
                        },
                        {
                            term: 'Subscriptions',
                            link: '#'
                        },
                        {
                            term: 'Talen Workshops',
                            link: '#'
                        },
                        {
                            term: 'CPSC Certificates',
                            link: '#'
                        },
                        {
                            term: 'Ratings',
                            link: '#'
                        },
                        {
                            term: 'Shop Help',
                            link: '#'
                        },
                        {
                            term: 'Contact Us',
                            link: '#'
                        }
                    ]
                },
                fourthMenu: {
                    title: 'Sites',
                    listMenu: [
                        {
                            term: 'DC',
                            link: '#'
                        },
                        {
                            term: 'MAD Magazine',
                            link: '#'
                        },
                        {
                            term: 'DC Kids',
                            link: '#'
                        },
                        {
                            term: 'DC Universe',
                            link: '#'
                        },
                        {
                            term: 'DC Power Visa',
                            link: '#'
                        }
                    ]
                },
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

footer {
    background-color: $dark;
    padding: 2rem 0;
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    position: relative;
    .container {
        @include dflex;
        align-items: flex-start !important;
        gap: 2rem;
    }

    a {
        font-size: .8rem;
        color: $grey;

        &:hover {
            color: $white;
        }
    }
}

h4 {
    text-transform: uppercase;
    color: $white;
    font-weight: 800;
    font-size: .8rem;
    padding-bottom: .6rem;
}
.menu-block-1 {
    padding-bottom: 1rem;
}
.menu-block-2 {
    @include dflex;
    align-items: flex-start;
    gap: 2rem;
}
.img-overflow {
    position: absolute;
    overflow: hidden;
    width: 500px;
    top: 0;
    right: 20%;
    height: 100%;

    div {
        position: absolute;
        top: -25%;
    }
}
</style>