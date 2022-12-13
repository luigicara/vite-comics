<script>
export default {
    data() {
        return {
            categoriesCard: [
                {
                    title: 'Digital Comics',
                    img: '/img/buy-comics-digital-comics.png'
                },

                {
                    title: 'DC Merchandise',
                    img: '/img/buy-comics-merchandise.png'
                },

                {
                    title: 'Subscription',
                    img: '/img/buy-comics-subscriptions.png'
                },

                {
                    title: 'Comic Shop Locator',
                    img: '/img/buy-comics-shop-locator.png'
                },

                {
                    title: 'DC Power Visa',
                    img: '/img/buy-dc-power-visa.svg'
                },
            ]
        }
    }
}
</script>

<template>
    <section id="categories">
        <div class="container">
            <div v-for="card in categoriesCard" class="categories-card">
                <img :src="card.img" alt="img">
                <span>{{ card.title.toUpperCase() }}</span>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../../styles/partials/_mixins.scss" as *;
@use "../../styles/partials/_variables.scss" as *;

#categories {
    height: 8rem;
    background-color: $primaryColor;

    .container {
        @include space-between;
        padding: 1rem 0;
        height: 100%;

        .categories-card {
            line-height: 3rem;
            font-size: 0.7rem;
            color: white;

            img {
                height: 3.5rem;
                max-width: 3.5rem;
                float: left;
                margin-right: 1rem;
            }
        }
    }
}
</style>