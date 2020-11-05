<template>
  <v-app id="inspire">
    <v-app-bar
      :clipped-left="$vuetify.breakpoint.lgAndUp"
      app
      color="dark"
      dark
    >
      <!--      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />-->

      <v-toolbar-title style="width: 350px">
        <a href="/" class="white--text" style="text-decoration: none">
          <v-icon>mdi-owl</v-icon>&nbsp;Workation
        </a>
      </v-toolbar-title>
      <v-spacer />
      <v-btn href="/signin" icon>
        <v-icon>mdi-account-circle</v-icon>
      </v-btn>
      <!-- <v-btn v-on="on" icon>
        <v-badge content="2" value="2" color="green" overlap>
          <v-icon>mdi-bell</v-icon>
        </v-badge>
      </v-btn>-->
      <v-btn href="/cart" icon>
        <v-badge content="2" value="2" color="primary" overlap>
          <v-icon>mdi-cart</v-icon>
        </v-badge>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-spacer></v-spacer>
      <nuxt />
    </v-main>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      items: [
        { title: "Tokyo" },
        { title: "New York" },
        { title: "London" },
        { title: "Berlin" },
        { title: "Beijing" }
      ],
      activeBtn: 1
    };
  }
};
</script>
