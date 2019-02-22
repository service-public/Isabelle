<template>
  <div class="isabelle">
    <Header/>
    <Selection/>
  </div>
</template>

<script>
import Header from './Header.vue'
import Selection from './Selection.vue'

export default {
  name: 'Isabelle',
  components:{
    Header, Selection
  },
  props: {
  }
}
</script>

<style scoped>
</style>
