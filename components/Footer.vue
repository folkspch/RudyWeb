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
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link }}
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
      links: [
        'Home',
        'About Us',
        'Services',
        'Contact Us',
      ],
    }),
}
</script>

<style scoped>
.footer-license{
    font-size: 0.8em;
    margin-bottom: 1em;
}
</style>