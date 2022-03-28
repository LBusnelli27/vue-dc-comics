<template>
  <div class="header">
    <img src="../assets/img/dc-logo.png" alt="Logo DC Comics Header">

    <div class="nav-container">
      <ul>
        <li v-for="(element, index) in navHeaderElement" :key="index">
          <a :href="element.href">{{ element.text }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'indexHeader',
  data : function() {
    return {
      navHeaderElement : [
        {
          text: "Characters",
          href: "#",
          active: false
        },
        {
          text: "Comics",
          href: "#",
          active: true
        },
        {
          text: "Movies",
          href: "#",
          active: false
        },
        {
          text: "Tv",
          href: "#",
          active: false
        },
        {
          text: "Games",
          href: "#",
          active: false
        },
        {
          text: "Collectibles",
          href: "#",
          active: false
        },
        {
          text: "Videos",
          href: "#",
          active: false
        },
        {
          text: "Fans",
          href: "#",
          active: false
        },
        {
          text: "News",
          href: "#",
          active: false
        },
        {
          text: "Shop",
          href: "#",
          active: false
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/scss/style.scss";

  .header{
    @include centerContentInDiv;
    display: flex;
    justify-content: space-between;
    padding: 1rem 0;
    height: 10vh;

    .nav-container {
      @include centerContentInDiv;
      height: 100%;
      ul{
        display: flex;
        li {
          padding: 0 .6rem;
          text-transform: uppercase;
          font-size: .8rem;
          &:hover {
            border-bottom: 3px solid $mainColor;
          }
        }
      }
    }
  }
</style>
