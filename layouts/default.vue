<template>
  <v-app>
    <v-app-bar
      fixed
      app
      color="white"
    >
      <v-toolbar-title>
        <v-img
          max-height="60"
          max-width="110"
          contain
          :src="require('@/assets/img/logo.png')"
        ></v-img>
      </v-toolbar-title>
      <v-spacer />
      <v-btn text color="primary">
        Beranda
      </v-btn>
      <v-btn text color="accent">
        Tentang
      </v-btn>
      <v-btn text color="accent">
        Kontak
      </v-btn>
      <v-btn text color="accent">
        Blog
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    
    <v-footer
      :absolute="true"
      app
    >
      <div class="mx-auto">        
        <span>Copyright</span>
        <span>&copy; {{ new Date().getFullYear() }}</span>
        <span class="ml-3">REDROOFED - House of English</span>
      </div>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      title: 'RedRoofed'
    }
  }
}
</script>
