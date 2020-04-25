<template>
       <v-card
            max-width="100%"
            height="auto"
            class="pt-4"
            @mouseenter="hover = true"
            @mouseleave="hover = false"
            :flat="!hover || $vuetify.breakpoint.smAndDown"
            style="background-color: #F5F3F3"
            :shaped="hover || $vuetify.breakpoint.smAndDown"
            :elevation="hover ? 10 : $vuetify.breakpoint.smAndDown ? 5 : 0"
        >
            <v-tooltip v-model="hover" top>
                <template v-slot:activator="{ on }">
                    <v-img
                    :src="tech.image"
                    :height="$vuetify.breakpoint.smAndDown ? 30 : 50" 
                    contain
                    v-on="on"
                    >
                    </v-img>
                </template>
                <span>{{tech.description}}</span>
            </v-tooltip>
          
            
            
            <v-list-item :dense="$vuetify.breakpoint.smAndDown">
              <v-list-item-content>
                <v-list-item-title class=" text-center" :class="$vuetify.breakpoint.smAndDown ? 'subtitle-1' : 'headline'">{{tech.name}}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>

            <v-card-actions style="justify-content:center">
              <span class="d-inline-block" v-if="!$vuetify.breakpoint.smAndDown">{{$t('technologies-content.tech-cards.expertise')}}:</span>
              <v-rating
                v-model="tech.skill"
                background-color="cyan lighten-3"
                color="cyan"
                readonly
                :dense="$vuetify.breakpoint.smAndDown"
                :small="!$vuetify.breakpoint.smAndDown"
                :x-small="$vuetify.breakpoint.smAndDown"
                full-icon="fas fa-circle"
                empty-icon="far fa-circle"
              ></v-rating>
            </v-card-actions>
          </v-card>
</template>

<script>
export default {
    props: ['tech'],
    data() {
        return {
            hover: false
        }
    },
}
</script>