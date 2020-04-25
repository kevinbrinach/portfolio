<template>
  <div class="background" :style="$vuetify.breakpoint.smAndDown ? 'height:300px' : 'height:500px'">
    <v-layout fill-height align-center>
      <v-container>
        <v-row align="center" justify="center" class="white--text text-center">
          <v-col cols="12">
            <div class=" font-weight-bold" :class="$vuetify.breakpoint.smAndDown ? 'headline' : 'display-2'">{{text1}}</div>
            <div :class="$vuetify.breakpoint.smAndDown ? 'title' : 'headline'">{{text}}</div>
          </v-col>
        </v-row>
      </v-container>
    </v-layout>
  </div>
</template>

<script>
export default {
  props: ['text1', 'text']
}
</script>

<style lang="scss">
  /* .background {
	background-image: linear-gradient(to right, rgb(76, 76, 76) 0%, rgb(89, 89, 89) 12%, rgb(102, 102, 102) 25%, rgb(0, 0, 0) 39%, rgb(71, 71, 71) 51%, rgb(17, 17, 17) 60%, rgb(44, 44, 44) 77%, rgb(43, 43, 43) 88%, rgb(28, 28, 28) 91%, rgb(19, 19, 19) 100%);
} */
.background {
	background-image: linear-gradient(to right, rgb(76, 76, 76) 0%, rgb(102, 102, 102) 10%, rgb(89, 89, 89) 18%, rgb(17, 17, 17) 28%, rgb(71, 71, 71) 39%, rgb(0, 0, 0) 49%, rgb(44, 44, 44) 60%, rgb(28, 28, 28) 65%, rgb(28, 28, 28) 74%, rgb(43, 43, 43) 82%, rgb(19, 19, 19) 100%);

}
</style>