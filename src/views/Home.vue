<template>
  <div class="home" justify="center">
    <bg-image :text1="text1" :text="text"/>
    <v-container class="mb-6">
      <div class="text-center   grey--text text--darken-3" :class="$vuetify.breakpoint.smAndDown ? 'title my-2' : 'display-1 mb-4 mt-6'">About me</div>
      <v-row sm="12" md="4"  class="text-justify" justify="center">
        <v-col cols="12" md="10" lg="8"  class="" :class="$vuetify.breakpoint.smAndDown ? 'caption' : 'subtitle-1'">My name is Kevin Brinach I'm 27 years old. Over the past three years I've been working as a freelance web developer -frontend mostly- building websites with frameworks based on JavaScript, like React.JS and Vue.JS. And of course I also use CSS, HTML5 and other technologies that you can see in the aforementioned section.  </v-col>
        <v-col cols="12" md="10" lg="8" class="" :class="$vuetify.breakpoint.smAndDown ? 'caption' : 'subtitle-1'">My hobbies range from sports to videogames and series. When I'm not programming I'm always doing something. Boredom doesn't exist for me.</v-col>
        <v-col cols="12" md="10" lg="8" class="" :class="$vuetify.breakpoint.smAndDown ? 'caption' : 'subtitle-1'">I'm very passionate about programming and learning about said subject and I usually don't stop programming 'till the job is done.</v-col>
        <v-col cols="12" md="10" lg="8" class="" :class="$vuetify.breakpoint.smAndDown ? 'caption' : 'subtitle-1'">If you have a project I can help with, please get in touch.</v-col>
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
      text1 : 'Welcome to my page',
      text: 'I make web apps'
    }
  },
}
</script>
