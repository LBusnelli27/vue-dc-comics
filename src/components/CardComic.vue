<template>
  <div class="comic-element">
    <img :src="bookObj.thumb" :alt="bookObj.series">
    <p>{{ bookObj.series }}</p>
  </div>
</template>

<script>
export default {
  name: 'CardComic',
  props: ['bookObj']
}
</script>

<style lang="scss" scoped>
  .comic-element {
    width: calc((100% / 6) - 1.5rem);
    img{
      width: 100%;
    }
    p{
      color: white;
      text-transform: uppercase;
      font-size: .8rem;
    }
  }
</style>