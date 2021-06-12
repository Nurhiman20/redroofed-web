<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      fixed
      app
      color="white"
    >
      <v-toolbar-title>
        <v-img
          max-height="50"
          max-width="110"
          contain
          :src="require('@/assets/img/logo.png')"
        ></v-img>
      </v-toolbar-title>
      <v-spacer />
      <v-btn text color="primary" class="hidden-sm-and-down">
        Beranda
      </v-btn>
      <v-btn text color="accent" class="hidden-sm-and-down">
        Tentang
      </v-btn>
      <v-btn text color="accent" class="hidden-sm-and-down">
        Kontak
      </v-btn>
      <v-btn text color="accent" class="hidden-sm-and-down">
        Blog
      </v-btn>
      <v-app-bar-nav-icon class="hidden-md-and-up" color="primary" @click.stop="drawer = !drawer" />
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
      title: 'RedRoofed',
      drawer: false,
      clipped: false,      
      items: [
        {
          title: 'Beranda',
          to: '/'
        },
        {
          title: 'Tentang',
          to: '/tentang'
        },
        {
          title: 'Kontak',
          to: '/kontak'
        },
        {
          title: 'Blog',
          to: '/blog'
        }
      ]
    }
  }
}
</script>
