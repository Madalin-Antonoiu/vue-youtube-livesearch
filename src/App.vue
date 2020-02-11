<template>
  <div id="app">
    <YoutubeSearch/>
  </div>
</template>

<script>
import YoutubeSearch from './components/YoutubeSearch';

export default {
  name: 'app',
  components: {
    YoutubeSearch
  }
}
</script>

<style lang="css">
  #app{
    width:100%;
    max-width:550px;
    margin:0 auto;
  }
 

</style>