<template>
  <div class="home" justify="center">
    <bg-image :text1="$t('banner.home.main-text-home')" :text="$t('banner.home.secondary-text-home')"/>
    <v-container class="mb-6">
      <div class="text-center   grey--text text--darken-3" :class="$vuetify.breakpoint.smAndDown ? 'title my-2' : 'display-1 mb-4 mt-6'">{{$t ('home-content.about')}}</div>
      <v-row sm="12" md="4"  class="text-justify" justify="center">
        <v-col cols="12" md="10" lg="8"  class="" :class="$vuetify.breakpoint.smAndDown ? 'caption' : 'subtitle-1'">{{$t ('home-content.content-1')}}</v-col>
        <v-col cols="12" md="10" lg="8" class="" :class="$vuetify.breakpoint.smAndDown ? 'caption' : 'subtitle-1'">{{$t ('home-content.content-2')}}</v-col>
        <v-col cols="12" md="10" lg="8" class="" :class="$vuetify.breakpoint.smAndDown ? 'caption' : 'subtitle-1'">{{$t ('home-content.content-3')}}</v-col>
        <v-col cols="12" md="10" lg="8" class="" :class="$vuetify.breakpoint.smAndDown ? 'caption' : 'subtitle-1'">{{$t ('home-content.content-4')}}</v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import BgImage from '../components/BgImage.vue'


export default {
  components: {
    BgImage,
  },
  data() {
    return {
      text1 : 'Welcome to my page',
      text: 'I make web apps'
    }
  },
}
</script>
