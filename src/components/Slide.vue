<template>
  <div class="fixed" v-bind:style="style">
    <h1>{{title}}</h1>
    <p>{{content}}</p>
  </div>

</template>
<script>

export default {
  name: 'slidePage',
  data: function () {
    return {
      style: {
        'background': 'url("static/img/' + this.backgroundImage + '") center center no-repeat',
        'background-size': 'cover',
        'width': this.width,
        'height': this.height
      }
    }
  },
  props: ['title', 'content', 'width', 'height', 'backgroundImage']

}
</script>
