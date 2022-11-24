<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed right app>
      <div style="padding:50px">
        <nuxt-link to="/">Inspira't</nuxt-link>
        <br>
        <nuxt-link to="/casos-exit">Casos d'èxit</nuxt-link>
        <br>
        <nuxt-link to="/contacte">Contacte</nuxt-link>
      </div>
    </v-navigation-drawer>
    <v-app-bar flat :clipped-left="clipped" fixed app>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <div class="hidden-sm-and-down">
        <v-btn to="/" text>Inspira't</v-btn>
        <v-btn to="/casos-exit" text>Casos d'èxit</v-btn>
        <v-btn to="/contacte" color="black" dark>Contacte</v-btn>
        <v-btn to="/numeros" color="black" dark>Numeros</v-btn>
      </div>
      <v-app-bar-nav-icon class="hidden-md-and-up" @click.stop="drawer = !drawer" />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-navigation-drawer v-model="rightDrawer" :right="right" temporary fixed>
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-magnify',
          title: "Cerca",
          to: "/cerca"
        },
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
      title: 'Exercici Navegació'
    }
  }
}
</script>
