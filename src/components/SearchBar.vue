<template>
  <div class="search-bar">
    <input type="text" placeholder="Search Youtube here" v-model="searchKeyword" @input="searchKeywordChange">
   </div>
</template>

<script>
import _ from 'lodash';

export default {
  name: 'Header',
  data() {
    return {
      // Placholder text on init search
      searchKeyword: 'orez cu lapte'
    }
  },
  methods: {
    // use Lodash debounce to throttle search rendering/reloading (400 milliseconds)
    searchKeywordChange: _.debounce( function () {
      //  pass event up to parent App.vue
      this.$emit('termChange', this.searchKeyword);
    }, 400)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.search-bar{
  display:block;
  margin: 0 auto;
}

</style>
