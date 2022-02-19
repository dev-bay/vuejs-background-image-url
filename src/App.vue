<template>
  <div id="app">
    <SingleNewsBlock v-for="(news, i) in newsData" :key="i" :news="news" />
    <footer>
      <small>
        * Photos from wikipedia: <a href="https://pl.wikipedia.org/wiki/Wroc%C5%82aw" target="_blank">Wroclaw</a>
      </small>
    </footer>
  </div>
</template>

<script>
import SingleNewsBlock from './components/SingleNewsBlock.vue'

export default {
  name: 'App',
  components: {
    SingleNewsBlock
  },
data () {
  return {
    newsData: [{
      img: 'bridge.png',
      title: "Bridge at night",
      desc: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec ullamcorper aliquet nulla a aliquam. Quisque sit amet fringilla justo. Cras ornare massa at dolor feugiat facilisis sed quis nunc. Suspendisse placerat euismod dictum.'
    }, {
      img: 'bridge2.png',
      title: "Highway bridge",
      desc: 'Duis placerat fermentum ipsum, nec vulputate mi blandit condimentum. In hac habitasse platea dictumst.'
    }, {
      img: 'building.png',
      title: "Historic building",
      desc: 'Vestibulum ac purus suscipit, aliquam nisi et, luctus arcu. Nam eget maximus est. Etiam sit amet accumsan arcu, ut imperdiet diam. Nulla facilisi'
    }, {
      img: 'skyscraper.png',
      title: "Skyscraper",
      desc: 'Aenean efficitur et ex vel luctus. Quisque commodo vel ex id consectetur. Sed vitae quam bibendum lectus tristique ultrices.'
    }]
  }
}
}
</script>

<style>
#app {
  width: 500px;
  margin: 0 auto;
}
</style>
