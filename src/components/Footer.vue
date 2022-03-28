<template>
  <div class="footer">
    <section class="top-part-footer">
      <img src="../assets/img/footer-bg.jpg" alt="Background footer img">
      <div class="footer-container-list">
        <div>
          <div></div>
          <div></div>
          <div></div>
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
    .footer-container-list {
      img {
        position: absolute;
        top: -40px;
        right: 70px;
        height: 500px;
      }
    }
  }
</style>