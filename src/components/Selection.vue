<template>
  <div class="selection">
    <Card v-for="feature in features" :feature="feature" :key="feature.key"/>
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
          key: 0,
          name: "EDT",
          icon: "fa-calendar-alt"
        },
        {
          key: 1,
          name: "Cours",
          icon: "fa-pen-nib"
        },
        {
          key: 2,
          name: "Notes",
          icon: "fa-file-medical-alt"
        },
      ]
    }
  }
}
</script>

<style scoped>
  .selection{
    display: flex;
    flex-direction: row;
  }
</style>
