<template>
  <div class="news-block">
    <div class="news-img" :style="backgroundImageInlineStyle">
      <h2>{{news.title}}</h2>
    </div>
    <div class="news-description">
      {{news.desc}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'SingleNewsBlock',
  props: {
    news: Array
  },
  computed: {
    backgroundImageInlineStyle () {
      return `background-image: url("./assets/${this.news.img}");`;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  /**
  * BACKGROUND IMAGE URL ELEMENT'S STYLES - BEGINING 
  * POSITION BACKGROUND IMAGE TO ALWAYS COVER WHOLE BLOCK ELEMENT
  * AND POSITION IT IN CENTER
  * BACKGROUND IMAGE URL IS ADDED AS INLINE STYLE TO EACH ELEMENT IN HTML CODE ABOVE
  */
  .news-img {
    height: 200px;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
  }
  /* BACKGROUND IMAGE URL ELEMENT'S STYLES - END */

  .news-block {
    background: orange;
    width: 240px;
    display: inline-block;
    margin: 10px 5px;
    padding: 5px;
    box-sizing: border-box;
    vertical-align: top;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  .news-block h2 {
    margin: 0;
    text-align: center;
    color: #fff;
    text-shadow: 0 0 2px #000;;
  }
  .news-description {
    padding: 5px;
  }
</style>
