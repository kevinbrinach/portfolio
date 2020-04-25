<template>
  <v-app-bar :dense="$vuetify.breakpoint.smAndDown" absolute color="transparent" dark class="">
          <v-app-bar-nav-icon @click="showMenu = !showMenu" v-if="$vuetify.breakpoint.smAndDown"></v-app-bar-nav-icon>
          <v-avatar class="mr-2" size="40">
            <img
              src="../assets/avatar.png"
              alt="Kevin"
              v-if="!$vuetify.breakpoint.smAndDown"
            >
          </v-avatar>
          <v-toolbar-title class="display-1 font-weight-bold" v-if="!$vuetify.breakpoint.smAndDown">Kevin Brinach</v-toolbar-title>
          <v-spacer  v-if="$vuetify.breakpoint.smAndDown"></v-spacer>
          <v-toolbar-title class="headline font-weight-bold" v-if="$vuetify.breakpoint.smAndDown" style="right: 20px; position: absolute">Kevin Brinach</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-toolbar-items v-if="!$vuetify.breakpoint.smAndDown">
            <v-btn to="/" text >Home</v-btn>
            <v-btn to="/technologies" text >Technologies</v-btn>
            <v-btn to="/projects" text >Projects</v-btn>
            <v-btn to="/contact" text >Contact Info</v-btn>
          </v-toolbar-items>

          <v-navigation-drawer
            v-model="showMenu"
            hide-overlay
            app
            class="background"
            height="300"
            fixed
            style="text-align:left;"
          >
            <v-list
              dense
              nav
              class="py-0"
            >
              <v-list-item>
                <v-list-item-avatar>
                  <img src="../assets/avatar.png">
                </v-list-item-avatar>

                <v-list-item-content>
                  <v-list-item-title>Kevin Brinach - WebDev</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
            <v-list
              nav
            >
              <v-list-item>

                <v-list-item-content>
                  <v-btn to="/" text >Home</v-btn>
                  <v-btn to="/technologies" text >Technologies</v-btn>
                  <v-btn to="/projects" text >Projects</v-btn>
                  <v-btn to="/contact" text >Contact Info</v-btn>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-navigation-drawer>
          
  </v-app-bar>
</template>

<script>

export default {
  data() {
    return {
      options: {
        duration: 300,
        offset: 0,
        easing: "easeInOutCubic",
      },
      showMenu: false
    };
  },
};
</script>
</style>