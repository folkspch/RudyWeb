<template>
  <v-footer
    color="#3b6ab6"
    padless
  >
    <v-row
      justify="center"
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
    

      <v-col
        class="py-3 text-center white--text"
        cols="12"
        color="#3b6ab6"
      >

        <div class="footer-license">{{ new Date().getFullYear() }} © Rudy Technology Co., Ltd. All Rights Reserved.</div>

      </v-col>
    </v-row>
  </v-footer>
</template>

<script>
export default {
    data: () => ({
      links: {
        'Home': '/',
        'About Us': '/About',
        'Services': '/Service',
        'Contact Us': '/Contact',
      },
      
    }),
}
</script>

<style scoped>
.footer-license{
    font-size: 0.8em;
    margin-bottom: 1em;
}
.footer-btn{
  color: white;
  text-decoration: none;
}
</style>