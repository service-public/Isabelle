<template>
  <div class="card box button">
    <h1> {{ feature.name.toUpperCase() }} </h1>
    <i class="fas" :class="feature.icon"></i>
  </div>
</template>

<script>
export default {
  name: 'Card',
  components:{
  },
  props: [
    'feature'
  ]
}
</script>

<style scoped>
  *{
    text-align: center;
  }

  .card{
    min-width: 200px;
    max-width: 10%;
    min-height: 250px;
    max-height: 20vh;
  }

</style>
