<script>
  import Header from './components/HeaderApp.vue';
  import Content from './components/MainApp.vue';

  export default{
    components:{
      Header,
      Content,
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
  </main>
</template>

<style lang="scss" scoped>
  @use './styles/partials/variables.scss' as *;

  .content{
    background-color: $secondary;
    padding: 3rem;
  }
</style>