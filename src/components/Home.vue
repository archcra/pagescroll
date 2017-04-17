<template>
<div>

  <div class="section">
    <div class="oop"></div>
    <div class="fixed">
      <h1 class="large">{{title}}</h1>
      <p>{{subtitle}}</p>
    </div>
  </div>

  <div v-for="slide in slides" class="section">
    <slide-page 
    v-bind:title="slide.title"
    v-bind:content="slide.content"
    v-bind:width="slide.width"
    v-bind:height="slide.height"
    v-bind:backgroundImage="slide.image"
    ></slide-page>
  </div>


  <div class="section">
    <p class="fixed white">谢谢观赏<br/>Thanks for watching</p>
  </div>

</div>
</template>

<script>
var Slide = require('./Slide')
const storyData = require('json-loader!../assets/data/story.json')
export default {
  components: {
    slidePage: Slide
  },
  data: () => {
    return {
      slides: storyData.slides,
      title: storyData.cover.title,
      subtitle: storyData.cover.subtitle,
      pageTitle: storyData.pageTitle
    }
  },
  mounted: function () {
    document.title = this.pageTitle
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>@import '../assets/scss/parallax-background.scss'</style>
