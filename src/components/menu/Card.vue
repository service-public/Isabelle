<template>
  <div class="card box button" @click="goTo">
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
  ],
  methods: {
    goTo: function(){
      this.$emit("selection", this.feature.key)
    }
  }
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

    padding-top: 3vh;
    margin: 20px;
  }

  i{
    margin-top: 7vh;
    font-size: 50px;
  }

</style>
