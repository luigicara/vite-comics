<script>
export default {
  data() {
    return {
      navItems: ['CHARACTHERS', 'COMICS', 'MOVIES', 'TV', 'GAMES', 'COLLECTIBLES', 'VIDEOS', 'FANS', 'NEWS', 'SHOP']
    }
  },
}
</script>

<template>
  <div class="container">
    <header>
      <img src="/img/dc-logo.png" alt="logo">

      <nav>
        <ul>
          <li v-for="item in navItems">
            <a href="">
              {{ item }}
            </a>
          </li>
        </ul>
      </nav>

    </header>
  </div>

</template>

<style lang="scss" scoped>
@use "../styles/partials/_mixins.scss" as *;
@use "../styles/partials/_variables.scss" as *;

header {
  height: $headerHeight;
  @include space-between;

  img {
    max-height: 75%;
  }

  nav {
    height: 100%;

    ul {
      height: 100%;
      list-style: none;
      @include space-between;

      li {
        font-size: 0.6rem;
        font-weight: bold;
        margin: 0 1rem;
        height: 100%;

        @include vertical-align-middle($headerHeight);

        &:hover {
          border-bottom: 4px solid $primaryColor;

          a {
            color: $primaryColor;
          }
        }

        a {
          text-decoration: none;
          color: black;
        }
      }
    }
  }
}
</style>
