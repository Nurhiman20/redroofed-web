<template>
  <v-app>
    <v-app-bar
      fixed
      app
      color="white"
    >
      <v-toolbar-title v-text="title" />
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
      <span>&copy; {{ new Date().getFullYear() }}</span>
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
