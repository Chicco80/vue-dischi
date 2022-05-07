<template>
  <div id="app">
    <header>
      <AppHeader/>
    </header>
    <main>
      <AppMain/>
      <AppGrid/>
    </main>
  </div>
</template>

<script>

import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppGrid from './components/AppGrid.vue'


export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppGrid,
  }

}
</script>


<style lang="scss">
@import "@/assets/styles/general.scss";
  main{
    height: calc(100vh - 80px);
    padding-top: 100px;
}

</style>
