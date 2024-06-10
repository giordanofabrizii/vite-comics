<script>
  import Header from './components/HeaderApp.vue';
  import Content from './components/MainApp.vue';
  import MainNav from './components/NavMainApp.vue';
  import FooterNav from './components/FooterNav.vue';
  import Socials from './components/Socials.vue';

  export default{
    components:{
      Header,
      Content,
      MainNav,
      FooterNav,
      Socials,
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
  <footer>
    <div class="jumbo">
      <FooterNav/>
    </div>
    <Socials/>
  </footer>
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

  footer{
    background-color: #303030;

    .jumbo {
      background-image: url(./assets/img/footer-bg.jpg);
      background-repeat: no-repeat;
      background-size: cover;
    }
  }


</style>