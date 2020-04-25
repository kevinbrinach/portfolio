<template>
  <div>
    <bg-image :text1="text1"/>
    <v-container justify="center">
      <div class="text-center  my-6 grey--text text--darken-3" :class="$vuetify.breakpoint.smAndDown ? 'title text-justify' : 'headline' ">Listed below are the technologies I usually use and my expertise on them</div>
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
          description: 'I develop most of my work using Vue.js'
        },
        {
          name: 'React',
          image: 'https://cdn.worldvectorlogo.com/logos/react-2.svg',
          skill: 4,
          description: 'I started making web apps in React'
        },
        {
          name: 'HTML5',
          image: 'https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg',
          skill: 5,
          description: 'All my work relies on HTML5'
        },
        {
          name: 'JavaScript',
          image: 'https://cdn.worldvectorlogo.com/logos/javascript.svg',
          skill: 4,
          description: 'JavaScript was one of the first languages I learned'
        },
        {
          name: 'Vuetify',
          image: 'https://cdn.worldvectorlogo.com/logos/vuetify.svg',
          skill: 3,
          description: 'I usually use Vuetify for its sweet Material Design components'
        },
        {
          name: 'Bootstrap',
          image: 'https://cdn.worldvectorlogo.com/logos/bootstrap-4.svg',
          skill: 3,
          description: 'Bootstrap is the first CSS framework that I used'
        },
        {
          name: 'CSS3',
          image: 'https://cdn.worldvectorlogo.com/logos/css-5.svg',
          skill: 3,
          description: "I don't rely only on CSS frameworks"
        },
        {
          name: 'Quasar.js',
          image: 'https://cdn.quasar.dev/logo/svg/quasar-logo.svg',
          skill: 4,
          description: 'Quasar makes my life so much easier'
        },
        {
          name: 'Redux',
          image: 'https://cdn.worldvectorlogo.com/logos/redux.svg',
          skill: 3,
          description: "I use Redux for its single state"
        },
        {
          name: 'Vuex',
          image: 'https://user-images.githubusercontent.com/7110136/29002857-9e802f08-7ab4-11e7-9c31-604b5d0d0c19.png',
          skill: 4,
          description: 'I use Vuex for its single state'
        },
        {
          name: 'Firebase',
          image: 'https://cdn.worldvectorlogo.com/logos/firebase-1.svg',
          skill: 3,
          description: "I've used Firebase and Firestore in some projects"
        },
        {
          name: 'Docker',
          image: 'https://cdn.worldvectorlogo.com/logos/docker.svg',
          skill: 2,
          description: "I'm in the process of getting used to Docker"
        },
        {
          name: 'Node JS',
          image: 'https://cdn.worldvectorlogo.com/logos/nodejs.svg',
          skill: 2,
          description: "I developed a REST API using Node JS along Express JS"
        },
        {
          name: 'MongoDB',
          image: 'https://cdn.worldvectorlogo.com/logos/mongodb.svg',
          skill: 3,
          description: 'At college my peers and I used MongoDB to manage NoSQL databases'
        },
        {
          name: 'GitHub',
          image: 'https://cdn.worldvectorlogo.com/logos/github-1.svg',
          skill: 4,
          description: "I have my public repositories in GitHub"
        },
        
        {
          name: 'GitLab',
          image: 'https://cdn.worldvectorlogo.com/logos/gitlab.svg',
          skill: 4,
          description: "My private repositories are here"
        },
        
        {
          name: 'BitBucket',
          image: 'https://cdn.worldvectorlogo.com/logos/bitbucket-icon.svg',
          skill: 4,
          description: "My private repositories are here"
        },
        {
          name: 'Trello',
          image: 'https://cdn.worldvectorlogo.com/logos/trello.svg',
          skill: 5,
          description: 'I arrange my tasks in a project using Trello'
        },
        {
          name: 'Jira',
          image: 'https://cdn.worldvectorlogo.com/logos/jira-3.svg',
          skill: 5,
          description: 'I arrange my tasks in a project using Jira'
        },
        {
          name: 'MySQL',
          image: 'https://cdn.worldvectorlogo.com/logos/mysql.svg',
          skill: 3,
          description: 'Management of relational databases at collegue'
        },
        {
          name: 'Laravel PHP',
          image: 'https://cdn.worldvectorlogo.com/logos/laravel-2.svg',
          skill: 2,
          description: 'In the process of learning'
        },
      ]
    }
  },
}
</script>
