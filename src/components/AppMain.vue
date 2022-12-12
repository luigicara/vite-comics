<script>
export default {
    data() {
        return {
            categoriesCard: [
                {
                    title: 'Digital Comics',
                    img: '/public/img/buy-comics-digital-comics.png'
                },

                {
                    title: 'DC Merchandise',
                    img: '/public/img/buy-comics-merchandise.png'
                },

                {
                    title: 'Subscription',
                    img: '/public/img/buy-comics-subscriptions.png'
                },

                {
                    title: 'Comic Shop Locator',
                    img: '/public/img/buy-comics-shop-locator.png'
                },

                {
                    title: 'DC Power Visa',
                    img: '/public/img/buy-dc-power-visa.svg'
                },
            ]
        }
    }
}
</script>

<template>
    <main>
        <section id="content">
            <div class="container">
                <p>-->Content goes here&lt;-- </p>
            </div>
        </section>

        <section id="categories">
            <div class="container">
                <div v-for="card in categoriesCard" class="categories-card">
                    <img :src="card.img" alt="img">
                    <span>{{ card.title.toUpperCase() }}</span>
                </div>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_mixins.scss" as *;
@use "../styles/partials/_variables.scss" as *;

#content {
    height: $sectionHeight;
    background-color: black;
}

p {
    line-height: $sectionHeight;
    color: white;
    font-weight: bold;
    font-size: 1.5rem;
}

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
                height: 3rem;
                max-width: 3rem;
                float: left;
                margin-right: 1rem;
            }
        }
    }
}
</style>