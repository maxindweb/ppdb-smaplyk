<template>
  <v-app>
    <div>
      <v-app-bar flat dark>
      <v-app-title>
        <span>PPDB SMA Pangudi Luhur</span>
      </v-app-title>
      <v-spacer></v-spacer>
      <div class="hidden-sm-and-down">
        <v-btn text to="/">
          <span>Home</span>
        </v-btn>
        <v-btn text to="/information">
          <span>Informasi</span>
        </v-btn>
        <v-btn text to="help">
          <span>Bantuan</span>
          <!-- <v-icon>mdi-help</v-icon> -->
        </v-btn>
        <v-btn outlined rounded  color="info" to="/login">
          Login
          <v-icon>mdi-login</v-icon>
        </v-btn>
      </div>
      <v-app-bar-nav-icon 
      class="hidden-md-and-up" 
      temporary
      absolute
      right
      @click.stop="drawer =!drawer"
      >
      </v-app-bar-nav-icon>
      
    </v-app-bar>
    <v-navigation-drawer
    v-model="drawer"
    absolute
    right
    temporary
    >
      <v-list>
        <v-list-item
        v-for="item in items"
        :key="item.title"
        >
        </v-list-item>  
      </v-list>
    </v-navigation-drawer>  
    </div>  
    <nuxt-child />
    <v-footer
      :absolute="!fixed"
      app
      class="pa-4"
    >
      <v-container>
        <v-row>
          <span>&copy; {{ new Date().getFullYear() }} SMA Pangudi Luhur Yogyakarta</span>
        </v-row>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
