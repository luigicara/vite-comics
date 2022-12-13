<script>
export default {
    data() {
        return {
            imgSrc: ['/img/footer-facebook.png', '/img/footer-twitter.png', '/img/footer-youtube.png', '/img/footer-pinterest.png', '/img/footer-periscope.png']
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <button>
                SIGN-UP NOW!
            </button>

            <div>
                <strong>FOLLOW US</strong>

                <a v-for="img in imgSrc" href="">
                    <img v-bind:src="img" alt="social">
                </a>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/_variables.scss" as *;
@use "../styles/partials/_mixins.scss" as *;

footer {
    height: $footerHeight;
    background-color: #303030;

    .container {
        height: 100%;
        @include space-between;

        button {
            color: white;
            font-size: 1rem;
            background-color: transparent;
            padding: 0.8rem;
            border: 2px solid $primaryColor;
        }

        div {
            color: $primaryColor;
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 1rem;

            a {
                display: inline-block;
            }
        }
    }
}
</style>