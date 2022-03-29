<template>
  <div class="main">
    <div class="comics-container">
      <div class="comics-library-container">
        <CardComic />
      </div>
    </div>
    <div class="comics-buy-container">
      <div class="div-container-element">
        <div class="element-comics-buy" v-for="(element, index) in mainNavBuyElement" :key="index">
          <img :src="'./img/' + element.imgName" :alt="element.text + ' img'">
          <p>{{ element.text }}</p>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>
import CardComic from './CardComic.vue';

export default {
  name : 'indexMain',
  components : {
    CardComic
  },
  data : function() {
    return {
      mainNavBuyElement : [
        {
          text: "Digital Comics",
          href: "#",
          imgName: "buy-comics-digital-comics.png"
        },
        {
          text: "Dc Merchndise",
          href: "#",
          imgName: "buy-comics-merchandise.png"
        },
        {
          text: "Subscription",
          href: "#",
          imgName: "buy-comics-subscriptions.png"
        },
        {
          text: "Comic Shop Locator",
          href: "#",
          imgName: "buy-comics-shop-locator.png"
        },
        {
          text: "DC Power Visa",
          href: "#",
          imgName: "buy-dc-power-visa.svg"
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/scss/style.scss";

  .comics-container {
    background-color: $bgBlack;
    .comics-library-container {
      @include withWebsite;
    }
  }

  .comics-buy-container {
    background-color: $mainColor;
    .div-container-element {
      @include withWebsite;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem;
      .element-comics-buy {
        display: flex;
        align-items: center;
        padding: 1rem;
        &:hover {
          transform: scale(1.05);
        }
        p {
          padding-left: .5rem;
          font-size: .7rem;
          font-weight: 700;
          color: white;
          text-transform: uppercase;
        }
        img {
          width: 50px;
          height: 60px;
        }
      }
    } 
  }
</style>