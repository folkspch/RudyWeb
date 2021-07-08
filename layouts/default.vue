<template>
<div>
<v-app class="page">
  
    <v-app-bar
      class="bar"
      absolute
      color="#3b6ab6"
      light
      shrink-on-scroll
      height="80em"
      scroll-target="#scrolling-techniques"
      app
    >
      
      <NuxtLink to="/"><img class="rudy_logo" src="../assets/rudy_logo.png"/></NuxtLink>
  <div class="nav-btn">
    <v-row
      
      no-gutters
    >
        <v-btn
          v-for="(link, text) in links" :key="text"
          text
          rounded
          class="my-2"
        >
          <NuxtLink :to="link" class="footer-btn"> {{ text }}</NuxtLink>

        </v-btn>
      </v-row>
  </div>
      
    </v-app-bar>
  
  <v-main >
      <v-container class="main">
        <nuxt />
      </v-container>
  </v-main>
  <Footer/>
</v-app>
</div>
  
</template>

<script>
import Footer from '@/components/Footer'
export default {
  data () {
    return {
      links: {
        'About Us': '/About',
        'Services': '/Service',
        'Contact Us': '/Contact',
      },
    }
  },
  components:{
    Footer
  }
}
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Prompt:wght@100;300;500&display=swap');
*{
  font-family: 'Prompt', sans-serif;
}
.page{
  background-color: white;
}
.main{
  max-width: 100%;
  padding: 0em;
  
}
.rudy_logo{
  height: 2.25em;
  width: 4.5em;
  margin-top: 0.3em;
}
.footer-btn {
  color: white;
  text-decoration: none;
  
}
.nav-btn{
  display: flex;
  width: 100%;

}
.row.no-gutters{
  justify-content: flex-end;
}
  
</style>
