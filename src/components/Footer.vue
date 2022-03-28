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
      <div class="container-bottom-footer">
        <div class="sing-up-footer">
          <button>Sing up now</button>
        </div>
        <div class="socials-footer">
          <h2>Follow us</h2>
          <img v-for="(element,index) in footerSocials" :key="index" :src="'./img/' + element.url" :alt="element.imgName">
        </div>
      </div>
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

      footerSocials : [
        {
          url: "footer-facebook.png",
          imgName: "Facebook link",
        },
        {
          url: "footer-periscope.png",
          imgName: "Periscope link",
        },
        {
          url: "footer-pinterest.png",
          imgName: "Pinterest link",
        },
        {
          url: "footer-twitter.png",
          imgName: "Twitter link",
        },
        {
          url: "footer-youtube.png",
          imgName: "Youtube link",
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  @import "../assets/scss/style.scss";

  .footer {
    position: relative;
  }
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
        gap: 4rem;
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

  .bottom-part-footer {
    width: 100%;
    height: 100%;
    background-color: $bgDarkGray;
    .container-bottom-footer{
      @include withWebsite;
      padding: 2rem 0;
      position: absolute;
      bottom: -50px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      .sing-up-footer {
        button {
          background-color: inherit;
          color: white;
          text-transform: uppercase;
          font-size: 1rem;
          padding: 1rem;
          font-weight: 600;
          border: 2px solid $mainColor;
        }
      }
      .socials-footer {

      }
    }
  }
</style>