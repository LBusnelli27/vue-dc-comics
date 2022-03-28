<template>
  <div class="footer">
    <section class="top-part-footer">
      <img class="bg-image-dc" src="../assets/img/footer-bg.jpg" alt="Background footer img">

      <div class="footer-container-list">
        <div class="list-side-footer">
          <div>
            <h2>Dc Comics</h2>
            <ul>
              <li v-for="(element, index) in footerDcComics" :key="index">
                <a :href="element.href">{{ element.text }}</a>
              </li>
            </ul>

            <h2>Shop</h2>
            <ul>
              <li v-for="(element, index) in footerShop" :key="index">
                <a :href="element.href">{{ element.text }}</a>
              </li>
            </ul>
          </div>
          <div>
            <h2>Dc</h2>
            <ul>
              <li v-for="(element, index) in footerDc" :key="index">
                <a :href="element.href">{{ element.text }}</a>
              </li>
            </ul>
          </div>
          <div>
            <h2>Sites</h2>
            <ul>
              <li v-for="(element, index) in footerSites" :key="index">
                <a :href="element.href">{{ element.text }}</a>
              </li>
            </ul>
          </div>
        </div>

        <img src="../assets/img/dc-logo-bg.png" alt="Background footer logo">
      </div>
    </section>

    <section class="bottom-part-footer">

    </section>
  </div>
</template>

<script>
export default {
  name : 'indexFooter',
  data : function() {
    return {
      footerDcComics : [
      {
          text: "Characters",
          href: "#",
        },
        {
          text: "Comics",
          href: "#",
        },
        {
          text: "Movies",
          href: "#",
        },
        {
          text: "Tv",
          href: "#",
        },
        {
          text: "Games",
          href: "#",
          
        },
        {
          text: "Videos",
          href: "#",
          
        },
        {
          text: "News",
          href: "#",
          
        },
      ],

      footerShop : [
        {
          text: "Shop DC",
          href: "#",
          
        },
        {
          text: "Shop DC Collectibles",
          href: "#",
          
        },
      ],

      footerDc: [
        {
          text: "Terms Of Use",
          href: "#",
          
        },
        {
          text: "Privacy policy (new)",
          href: "#",
          
        },
        {
          text: "Ad Choise",
          href: "#",
          
        },
        {
          text: "Advertising",
          href: "#",
          
        },
        {
          text: "Jobs",
          href: "#",
          
        },
        {
          text: "Subscriptions",
          href: "#",
          
        },
        {
          text: "Talent Workshops",
          href: "#",
          
        },
        {
          text: "CPSC Certificates",
          href: "#",
          
        },
        {
          text: "Ratings",
          href: "#",
          
        },
        {
          text: "Shop Help",
          href: "#",
          
        },
        {
          text: "Contact Us",
          href: "#",
          
        },
      ],

      footerSites : [
        {
          text: "DC",
          href: "#",
          
        },
        {
          text: "Mad Magazine",
          href: "#",
          
        },
        {
          text: "DC Kids",
          href: "#",
          
        },
        {
          text: "DC Universe",
          href: "#",
          
        },
        {
          text: "DC Power Visa",
          href: "#",
          
        },
      ],
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/scss/style.scss";

  .top-part-footer {
    position: relative;
    .bg-image-dc {
      width: 100%;
    }
    .footer-container-list {
      @include withWebsite;
      color: white;
      position: absolute;
      top: 50px;
      left: 100px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      .list-side-footer {
        display: flex;
        gap: 3.5rem;
        h2 {
          margin-top: 1rem;
          margin-bottom: .7rem;
          text-transform: uppercase;
        }
        li {
          margin-bottom: .4rem;
          a {
          color: #c8cdce;
          font-weight: 200;
        }
        }
      }
      img {
        height: 350px;
      }
    }
  }
</style>