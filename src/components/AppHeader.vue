<template>
<header>
  <nav class="navbar">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <img src="../assets/styles/spotify.png" alt="" width="30" height="24">
    </a>
  </div>
</nav>
</header>
</template>

<script>
export default {
  name: 'AppHeader',
 
}
</script>


<style scoped lang="scss">
@import "@/assets/styles/general.scss";

nav{
  height: 80px;
  background-color: $nav-color;
}
img{
  width: 60px;
  height: 50px;
}


</style>
