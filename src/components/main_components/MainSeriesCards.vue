<script>
import slidesJson from '../../assets/dc-comics.json'

export default {
    data() {
        return {
            slides: slidesJson
        }
    }
}
</script>

<template>
    <section class="jumbotron">
        <img src="/img/jumbotron.jpg" alt="jumbotron">
    </section>

    <section class="slides">
        <div class="container">
            <section class="cards">
                <div v-for="slide in slides" class="card">
                    <div>
                        <img :src="slide.thumb" alt="thumbnail">
                    </div>

                    <div class="series">
                        {{ slide.series.toUpperCase() }}
                    </div>
                </div>
            </section>
        </div>
    </section>

</template>

<style lang="scss" scoped>
.jumbotron {
    height: 400px;
    overflow: hidden;

    img {
        width: 100%;
        min-height: 100%;
    }
}

.slides {
    background-color: #1c1c1c;
    padding: 3rem 0;

    .cards {
        display: flex;
        flex-wrap: wrap;
        gap: 2rem 1rem;

        .card {
            max-width: calc((100% - 5rem) / 6);

            div {
                overflow: hidden;
                max-height: 12rem;

                img {
                    max-width: 100%;
                }
            }

            .series {
                color: white;
                margin: 1rem 0;
                font-size: 0.9rem;
            }

        }
    }
}
</style>