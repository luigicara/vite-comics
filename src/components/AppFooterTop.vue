<script>
export default {
    data() {
        return {
            footerEl: [
                {
                    title: 'DC Comics',
                    elements: [
                        'Characthers', 'Comics', 'TV', 'Games', 'Videos', 'News'
                    ]
                },

                {
                    title: 'Shop',
                    elements: [
                        'Shop DC', 'Shop DC Collectibles'
                    ]
                },

                {
                    title: 'DC',
                    elements: [
                        'Terms of Use', 'Privacy policy (New)', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact US'
                    ]
                },

                {
                    title: 'Sites',
                    elements: [
                        'DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'
                    ]
                },
            ]
        }
    }
}
</script>

<template>
    <section>
        <div class="container">
            <div class="left-col">
                <ul v-for="list in footerEl">
                    <strong>{{ list.title.toUpperCase() }}</strong>

                    <li v-for="element in list.elements">
                        <a href="">
                            {{ element }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
section {
    height: 400px;
    background-image: url('../../img/footer-bg.jpg');
    background-size: cover;

    .container {
        height: 100%;
        padding: 2rem 0;
        background: no-repeat right url('../../img/dc-logo-bg.png');

        .left-col {
            height: 100%;
            max-width: 400px;
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;

            ul {
                list-style: none;

                strong {
                    display: block;
                    margin: 1rem 0;
                    font-size: 1.1rem;
                    color: white;
                }

                li {
                    margin: 0.5rem 0;

                    a {
                        text-decoration: none;
                        font-size: 0.8rem;
                        color: grey;
                    }
                }
            }
        }
    }
}
</style>