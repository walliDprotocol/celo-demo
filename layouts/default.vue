<template>
  <v-app dark>
    <v-app-bar :clipped-left="clipped" fixed app>
      <v-toolbar-title v-text="title" />
      <v-spacer />

      <!-- <ui-connect-btn /> -->
      <!-- 
      <nuxt-link :to="'/creator'"> <v-btn> Create </v-btn> </nuxt-link>

      <nuxt-link :to="'/launcher'"><v-btn> Launch</v-btn> </nuxt-link> -->
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>

    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: "mdi-apps",
          title: "Dashboard",
          to: "/",
        },
        {
          icon: "mdi-apps",
          title: "Iframe laucher",
          to: "/launcher",
        },
        {
          icon: "mdi-apps",
          title: "Creator form",
          to: "/creator",
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: "WalliD WebApp",
    };
  },
};
</script>
