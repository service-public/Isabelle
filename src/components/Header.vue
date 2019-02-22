<template>
  <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
        <a class="navbar-item brand-text">
            <i class="fas fa-caret-left "></i> &nbsp;
            <h1>ISABELLE</h1>&nbsp;
            <img src="../assets/logo.png" alt="">
        </a>
    </div>

  <div class="navbar-menu">
    <div class="navbar-end">
      <div class="navbar-item">
        <button class= "button is-outlined is-big is-success" >Login</button>
      </div>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  name: 'Header',
  data: function(){
    return {
    }
  },
}
</script>

<style media="screen" scoped>
  #navbar{
    position: relative;
    left: 18vw;
  }
  #navbar *{
    padding-left: 50px;
    padding-right: 50px;
  }

</style>
