<script>
export default {
  data() {
    return {
      navItems: [
        {
          title: 'CHARACTHERS'
        },

        {
          title: 'COMICS'
        },

        {
          title: 'MOVIES'
        },

        {
          title: 'TV'
        },

        {
          title: 'GAMES'
        },

        {
          title: 'COLLECTIBLES'
        },

        {
          title: 'VIDEOS'
        },

        {
          title: 'FANS'
        },

        {
          title: 'NEWS'
        },

        {
          title: 'SHOP'
        },

      ]
    }
  },
}
</script>

<template>
  <header>
    <img src="/public/img/dc-logo.png" alt="">

    <nav>
      <ul>
        <li v-for="item in navItems">
          <a href="">
            {{ item.title }}
          </a>
        </li>
      </ul>
    </nav>
  </header>
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
        font-size: 0.5rem;
        margin: 0 1rem;
        height: 100%;

        @include vertical-align-middle($headerHeight);

        a {
          text-decoration: none;
          color: black;
        }
      }
    }
  }
}
</style>
