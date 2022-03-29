<template>
  <div class="main">
    <div class="comics-container">
      <div class="tag-current">Current Series</div>
      <div class="comics-library-container">
        <CardComic v-for="(element, index) in comicElements" :key="index" :bookObj="element" />
      </div>
      <button>Load more</button>
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
      ],

      comicElements : [
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$3.99",
          series: "Batman",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book"
        },
        {
          thumb: "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel"
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/scss/style.scss";

  .comics-container {
    position: relative;
    padding: 2rem 0;
    background-color: $bgBlack;
    display: flex;
    flex-direction: column;
    align-items: center;
    .tag-current {
      position: absolute;
      top: -30px;
      left: 9%;
      background-color: $mainColor;
      color: white;
      text-transform: uppercase;
      font-size: 1.2rem;
      padding: .8rem 2rem;
      font-weight: 600;
      border: none ;
    }
    .comics-library-container {
      @include withWebsite;
      display: flex;
      flex-wrap: wrap;
      gap: 1.5rem;
      padding: 2rem 0;
    }
    button {
      background-color: $mainColor;
      color: white;
      text-transform: uppercase;
      font-size: .8rem;
      padding: .8rem 2rem;
      font-weight: 600;
      border: none ;
      &:hover {
        transform: scale(1.05);
      }
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