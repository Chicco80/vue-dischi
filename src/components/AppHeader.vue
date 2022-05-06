<template>
<header>
  <nav class="navbar">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">
      <img src="/docs/5.0/assets/brand/bootstrap-logo.svg" alt="" width="30" height="24">
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
  background-color: $nav-color;
}

</style>
