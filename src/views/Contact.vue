<template>
  <div class="contact">
    <bg-image :text1="text1"/>
    <v-container>
      <div class="text-center my-6 grey--text text--darken-3" :class="$vuetify.breakpoint.smAndDown ? 'title' : 'headline' ">You can contact me on:</div>
      <v-row justify="center">
        <v-col lg="4" class="" v-for="(contact, index) in contactInfo" :key="index">
          <v-list-item :dense="$vuetify.breakpoint.smAndDown">
            <v-list-item-icon :class="$vuetify.breakpoint.smAndDown ? 'title' : 'headline mr-2' ">
              <v-btn :href="contact.url" icon  target="_blank">
                <v-icon :color="contact.color">{{contact.icon}}</v-icon>
              </v-btn>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title class="grey--text text--darken-1">{{contact.nick}}</v-list-item-title>
              <v-list-item-subtitle class="caption grey--text text--lighten-1">{{contact.name}}</v-list-item-subtitle>
            </v-list-item-content>
          </v-list-item>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import BgImage from '../components/BgImage.vue'

export default {
  components: {
    BgImage
  },
  data() {
      return {
          text1: 'How to Contact me',
          contactInfo: [
            {
              name: 'Email',
              url: 'mailto:kevinbrinach@hotmail.com',
              nick: 'kevinbrinach@hotmail.com',
              icon: 'fas fa-envelope',
              color: 'red darken-4'
            },
            {
              name: 'LinkedIn',
              url: 'https://www.linkedin.com/in/kevin-brinach/',
              nick: 'Kevin Brinach',
              icon: 'fab fa-linkedin',
              color: 'blue darken-2'
            },
            {
              name: 'GitHub',
              url: 'https://github.com/kevinbrinach/',
              nick: 'kevinbrinach',
              icon: 'fab fa-github-square',
              color: 'black'
            },
            {
              name: 'Facebook',
              url: 'https://www.facebook.com/kbrinach',
              nick: 'Kevin Brinach',
              icon: 'fab fa-facebook-square',
              color: 'blue darken-4'
            },
            {
              name: 'Instagram',
              url: 'https://www.instagram.com/kevinbrinach/',
              nick:'@kevinbrinach',
              icon: 'fab fa-instagram',
              color: 'red darken-2'
            },
            {
              name: 'Twitter',
              url: 'https://twitter.com/brinachjk',
              nick: '@brinachjk',
              icon: 'fab fa-twitter-square',
              color: 'blue'
            }
          ]
      }
  },
}
</script>