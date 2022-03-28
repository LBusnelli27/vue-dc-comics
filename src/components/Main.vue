<template>
  <div class="main">
    <div class="comics-container">
      <h2>---x  Content goes here  x---</h2>
    </div>
    <div class="comics-buy-container">
      <div v-for="(element, index) in mainNavBuyElement" :key="index">
        <img :src="'../assets/img/' + element.imgName" :alt="element.text + ' img'">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name : 'indexMain',
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
          imgName: "buy-comics-merhandise.png"
        },
        {
          text: "Subscription",
          href: "#",
          imgName: "buy-comics-subscription.png"
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
    h2{
      color: white;
      text-align: center;
      padding: 2rem;
    }
  }

  .comics-buy-container {
    background-color: $mainColor;
    display: flex;
  }
</style>