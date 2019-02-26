<template>
  <div class="isabelle">
    <Header @backToMenu="selection"/>

    <Selection v-if="!view" @selection="selection"/>
    <EDT v-if="view == 1"/>
    <Notes v-if="view == 3"/>

  </div>
</template>

<script>
import Header from './Header.vue'
import Selection from './menu/Selection.vue'
import EDT from './EDT/EDT.vue'
import Notes from './notes/Notes.vue'

export default {
  name: 'Isabelle',
  components:{
    Header, Selection, EDT, Notes
  },
  data: function(){
    return{
        view: 0
    }
  },
  props: {
  },
  methods:{
    selection: function(view){
      this.$data.view = view;
    }
  }
}
</script>

<style scoped>
</style>
