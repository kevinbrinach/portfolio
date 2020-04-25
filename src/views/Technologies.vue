<template>
  <div>
    <bg-image :text1="$t('banner.tech.main-text-tech')"/>
    <v-container justify="center">
      <div class="text-center  my-6 grey--text text--darken-3" :class="$vuetify.breakpoint.smAndDown ? 'title text-justify' : 'headline' ">{{$t('technologies-content.tech-header')}}</div>
      <v-row justify="center">
        <v-col cols="6" sm="4" lg="3" v-for="(tech, index) in technologies" :key="index" justify="center" class="">
          <tech-card :tech="tech"/>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import BgImage from '../components/BgImage.vue'
import TechCard from '../components/TechCard.vue'

export default {
  components: {
    BgImage,
    TechCard
  },
  data() {
    return {
      text1: 'Technologies I work with',
      technologies: [
        {
          name: 'Vue.js',
          image: 'https://cdn.worldvectorlogo.com/logos/vue-9.svg',
          skill: 5,
          description: this.$t('technologies-content.tech-cards.tooltips.vue')
        },
        {
          name: 'React',
          image: 'https://cdn.worldvectorlogo.com/logos/react-2.svg',
          skill: 4,
          description: this.$t('technologies-content.tech-cards.tooltips.react')
        },
        {
          name: 'HTML5',
          image: 'https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg',
          skill: 5,
          description: this.$t('technologies-content.tech-cards.tooltips.html5')
        },
        {
          name: 'JavaScript',
          image: 'https://cdn.worldvectorlogo.com/logos/javascript.svg',
          skill: 4,
          description: this.$t('technologies-content.tech-cards.tooltips.js')
        },
        {
          name: 'Vuetify',
          image: 'https://cdn.worldvectorlogo.com/logos/vuetify.svg',
          skill: 3,
          description: this.$t('technologies-content.tech-cards.tooltips.vuetify')
        },
        {
          name: 'Bootstrap',
          image: 'https://cdn.worldvectorlogo.com/logos/bootstrap-4.svg',
          skill: 3,
          description: this.$t('technologies-content.tech-cards.tooltips.bootstrap')
        },
        {
          name: 'CSS3',
          image: 'https://cdn.worldvectorlogo.com/logos/css-5.svg',
          skill: 3,
          description: this.$t('technologies-content.tech-cards.tooltips.css')
        },
        {
          name: 'Quasar.js',
          image: 'https://cdn.quasar.dev/logo/svg/quasar-logo.svg',
          skill: 4,
          description: this.$t('technologies-content.tech-cards.tooltips.quasar')
        },
        {
          name: 'Redux',
          image: 'https://cdn.worldvectorlogo.com/logos/redux.svg',
          skill: 3,
          description: this.$t('technologies-content.tech-cards.tooltips.redux')
        },
        {
          name: 'Vuex',
          image: 'https://user-images.githubusercontent.com/7110136/29002857-9e802f08-7ab4-11e7-9c31-604b5d0d0c19.png',
          skill: 4,
          description: this.$t('technologies-content.tech-cards.tooltips.vuex')
        },
        {
          name: 'Firebase',
          image: 'https://cdn.worldvectorlogo.com/logos/firebase-1.svg',
          skill: 3,
          description: this.$t('technologies-content.tech-cards.tooltips.firebase')
        },
        {
          name: 'Docker',
          image: 'https://cdn.worldvectorlogo.com/logos/docker.svg',
          skill: 2,
          description: this.$t('technologies-content.tech-cards.tooltips.docker')
        },
        {
          name: 'Node JS',
          image: 'https://cdn.worldvectorlogo.com/logos/nodejs.svg',
          skill: 2,
          description: this.$t('technologies-content.tech-cards.tooltips.node')
        },
        {
          name: 'MongoDB',
          image: 'https://cdn.worldvectorlogo.com/logos/mongodb.svg',
          skill: 3,
          description: this.$t('technologies-content.tech-cards.tooltips.mongo')
        },
        {
          name: 'GitHub',
          image: 'https://cdn.worldvectorlogo.com/logos/github-1.svg',
          skill: 4,
          description: this.$t('technologies-content.tech-cards.tooltips.github')
        },
        
        {
          name: 'GitLab',
          image: 'https://cdn.worldvectorlogo.com/logos/gitlab.svg',
          skill: 4,
          description: this.$t('technologies-content.tech-cards.tooltips.gitlab')
        },
        
        {
          name: 'BitBucket',
          image: 'https://cdn.worldvectorlogo.com/logos/bitbucket-icon.svg',
          skill: 4,
          description: this.$t('technologies-content.tech-cards.tooltips.bitbucket')
        },
        {
          name: 'Trello',
          image: 'https://cdn.worldvectorlogo.com/logos/trello.svg',
          skill: 5,
          description: this.$t('technologies-content.tech-cards.tooltips.trello')
        },
        {
          name: 'Jira',
          image: 'https://cdn.worldvectorlogo.com/logos/jira-3.svg',
          skill: 5,
          description: this.$t('technologies-content.tech-cards.tooltips.jira')
        },
        {
          name: 'MySQL',
          image: 'https://cdn.worldvectorlogo.com/logos/mysql.svg',
          skill: 3,
          description: this.$t('technologies-content.tech-cards.tooltips.sql')
        },
        {
          name: 'Laravel PHP',
          image: 'https://cdn.worldvectorlogo.com/logos/laravel-2.svg',
          skill: 2,
          description: this.$t('technologies-content.tech-cards.tooltips.laravel')
        },
      ]
    }
  },
  watch: {
    '$i18n.locale'() {
      this.technologies[0].description = this.$t('technologies-content.tech-cards.tooltips.vue')
      this.technologies[1].description = this.$t('technologies-content.tech-cards.tooltips.react')
      this.technologies[2].description = this.$t('technologies-content.tech-cards.tooltips.html5')
      this.technologies[3].description = this.$t('technologies-content.tech-cards.tooltips.js')
      this.technologies[4].description = this.$t('technologies-content.tech-cards.tooltips.vuetify')
      this.technologies[5].description = this.$t('technologies-content.tech-cards.tooltips.bootstrap')
      this.technologies[6].description = this.$t('technologies-content.tech-cards.tooltips.css')
      this.technologies[7].description = this.$t('technologies-content.tech-cards.tooltips.quasar')
      this.technologies[8].description = this.$t('technologies-content.tech-cards.tooltips.redux')
      this.technologies[9].description = this.$t('technologies-content.tech-cards.tooltips.vuex')
      this.technologies[10].description = this.$t('technologies-content.tech-cards.tooltips.firebase')
      this.technologies[11].description = this.$t('technologies-content.tech-cards.tooltips.docker')
      this.technologies[12].description = this.$t('technologies-content.tech-cards.tooltips.node')
      this.technologies[13].description = this.$t('technologies-content.tech-cards.tooltips.mongo')
      this.technologies[14].description = this.$t('technologies-content.tech-cards.tooltips.github')
      this.technologies[15].description = this.$t('technologies-content.tech-cards.tooltips.gitlab')
      this.technologies[16].description = this.$t('technologies-content.tech-cards.tooltips.bitbucket')
      this.technologies[17].description = this.$t('technologies-content.tech-cards.tooltips.trello')
      this.technologies[18].description = this.$t('technologies-content.tech-cards.tooltips.jira')
      this.technologies[19].description = this.$t('technologies-content.tech-cards.tooltips.sql')
      this.technologies[20].description = this.$t('technologies-content.tech-cards.tooltips.laravel')
    }
  },
}
</script>
