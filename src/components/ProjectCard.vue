<template>
    <v-row class="mb-6 grey lighten-5">
        <v-row lg="10" justify="center" :dense="$vuetify.breakpoint.smAndDown">
            <v-col cols="5" md="4" lg="4" v-for="(image, index) in project.images" :key="index">
                <v-card class="text-center" :href="image.image" target="_blank">
                    <v-img  :width="$vuetify.breakpoint.smAndDown ? 200 : $vuetify.breakpoint.mdAndDown ? 300 : 500" contain :height="$vuetify.breakpoint.smAndDown ? 150 : 300" :src="image.image" style="margin:auto"/>
                </v-card>
            </v-col>
        </v-row>
        <v-col cols="12" lg="12" class="text-left">
            <v-col class="grey--text text--darken-3" lg="12" :class="$vuetify.breakpoint.smAndDown ? 'body-2' : 'body-1'">{{$t('projects-content.name')}}</v-col>
            <v-col :class="$vuetify.breakpoint.smAndDown ? 'title pl-4' : 'ml-10 headline' " class="font-italic font-weight-bold  grey--text" lg="12">
                {{project.name}}
            </v-col>
            <v-col class="grey--text text--darken-3" lg="12" :class="$vuetify.breakpoint.smAndDown ? 'body-2' : 'body-1'">{{$t('projects-content.about')}}</v-col>
            <v-col class="text-justify" :class="$vuetify.breakpoint.smAndDown ? 'body-2 pl-5' : 'ml-10 body-1' " lg="12">
                {{project.about}}
            </v-col>
            <v-col class="grey--text text--darken-3" lg="12" :class="$vuetify.breakpoint.smAndDown ? 'body-2' : 'body-1'">{{$t('projects-content.tech')}}</v-col>
            <v-row :class="$vuetify.breakpoint.smAndDown ? 'px-8' : 'ml-10' " justify="start">
                <v-col cols="3" lg="1" v-for="(image, index) in project.technologies" :key="index" >
                    <v-tooltip bottom>
                        <template v-slot:activator="{ on }">
                            <v-img contain :width="$vuetify.breakpoint.smAndDown ? 50 : $vuetify.breakpoint.mdAndDown ? 60 : 80" :height="$vuetify.breakpoint.smAndDown ? 50 : 80" v-on="on" :src="image.img"></v-img>
                        </template>
                        <span>{{image.name}}</span>
                    </v-tooltip>
                </v-col>
            </v-row>

            <v-col class="grey--text text--darken-3" lg="12" :class="$vuetify.breakpoint.smAndDown ? 'body-2' : 'body-1'">{{$t('projects-content.site')}}</v-col>
            <v-col :class="$vuetify.breakpoint.smAndDown ? '' : 'ml-10' " lg="12">
                <a class="link" :class="$vuetify.breakpoint.smAndDown ? 'body-2 pl-4' : 'body-1'" :href="project.site" target="_blank">{{project.site ? project.name : 'N/A'}}</a>
            </v-col>
            
            <v-row v-if="project.repository">
                <v-col lg="12">Github:</v-col>
                <v-col lg="12">
                    <v-icon color="black" class="ml-10" size="50">fab fa-github</v-icon>
                </v-col>
                <v-col lg="12">{{project.repository}}</v-col>
            </v-row>
        </v-col>
    </v-row>
</template>

<script>
export default {
    props: ['project'],
}
</script>

<style lang="scss">
.link {
    color: grey !important
}
</style>