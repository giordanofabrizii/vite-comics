<script>
  import Header from './components/HeaderApp.vue';
  import Content from './components/MainApp.vue';
  import MainNav from './components/NavMainApp.vue';

  export default{
    components:{
      Header,
      Content,
      MainNav,
    }
  }
</script>

<template>
  <header>
    <Header/>
  </header>
  <main>
    <div class="content">
      <Content/>
    </div>
    <nav>
      <MainNav/>
    </nav>
  </main>
</template>

<style lang="scss" scoped>
  @use './styles/partials/variables.scss' as *;

  .content{
    background-color: $secondary;
    padding: 3rem;
  }

  nav{
    background-color: $primary;
    padding: 2rem;
  }
</style>