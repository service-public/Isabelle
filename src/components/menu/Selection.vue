<template>
  <div class="selection">
    <Card v-for="feature in features" :feature="feature" :key="feature.key" @selection="selection"/>
  </div>
</template>

<script>
import Card from './Card.vue'

export default {
  name: 'Selection',
  components:{
    Card
  },
  props: {
  },
  data: function(){
    return {
      features: [
        {
          key: 1,
          name: "EDT",
          icon: "fa-calendar-alt"
        },
        {
          key: 2,
          name: "Cours",
          icon: "fa-pen-nib"
        },
        {
          key: 3,
          name: "Notes",
          icon: "fa-file-medical-alt"
        },
      ]
    }
  },
  methods:{
    selection: function(view){
      this.$emit("selection", view);
    }
  }
}
</script>

<style scoped>
  .selection{
    display: flex;
    flex-direction: row;

    justify-content: center;

    padding-top: 10vh;
  }
</style>
