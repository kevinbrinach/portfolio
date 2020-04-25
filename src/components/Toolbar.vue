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
            <v-btn to="/" text >{{$t ('toolbar.home')}}</v-btn>
            <v-btn to="/technologies" text >{{$t ('toolbar.tech')}}</v-btn>
            <v-btn to="/projects" text >{{$t ('toolbar.projects')}}</v-btn>
            <v-btn to="/contact" text >{{$t ('toolbar.contact')}}</v-btn>
            <v-btn class="text-capitalize ml-6" small @click="changeLocale('en')" text v-if="$i18n.locale != 'en'"><flag iso="us" style="margin-right:10px"/>English</v-btn>
            <v-btn class="text-capitalize ml-6" small @click="changeLocale('es')" text v-if="$i18n.locale != 'es'"><flag iso="ar" />Español</v-btn>

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
                  <v-btn to="/" text >{{$t ('toolbar.home')}}</v-btn>
                  <v-btn to="/technologies" text >{{$t ('toolbar.tech')}}</v-btn>
                  <v-btn to="/projects" text >{{$t ('toolbar.projects')}}</v-btn>
                  <v-btn to="/contact" text >{{$t ('toolbar.contact')}}</v-btn>
                  <v-btn class="text-capitalize mt-10" small @click="changeLocale('en')" text v-if="$i18n.locale != 'en'"><flag iso="us" />English</v-btn>
                  <v-btn class="text-capitalize mt-10" small @click="changeLocale('es')" text v-if="$i18n.locale != 'es'"><flag iso="ar" />Español</v-btn>
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
      langs: ['en', 'es'],
      showMenu: false
    };
  },
  methods: {    
    changeLocale(locale) {
      this.$i18n.locale = locale;    
    }
  }
};
</script>

<style lang="scss">
.flag-icon {
 margin-right: 5px !important;
}  
</style>