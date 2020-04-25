<template>
  <div class="projects">
    <bg-image :text1="text1"/>
    <v-container lg="12">
        <div class="text-center mt-6 grey--text text--darken-3" :class="$vuetify.breakpoint.smAndDown ? 'title text-justify' : 'headline'">These are some of the projects that I worked on:</div>
        <!-- <div class="text-left caption mt-1 ">Bear in mind some of these are propietary software so its repositories won't be available</div> -->
        <v-row class="mt-5 pt-5">
            <v-col lg="12" v-for="project in projects" :key="project.id" class="grey--text">
                <project-card  :project="project"/>
                <v-divider light class="mb-6"></v-divider>
            </v-col>
        </v-row>
    </v-container>
  </div>
</template>

<script>
import BgImage from '../components/BgImage.vue'
import ProjectCard from '../components/ProjectCard.vue'


export default {
    components: {
        BgImage,
        ProjectCard
    },
    data() {
        return {
            text1: 'Projects I worked on',
            projects: [
                {
                    id: 6,
                    name: 'YouPoach',
                    about: 'Front-end for hiring platform for professionals and freelancers.',
                    images: [
                        {
                            id: 1,
                            image: 'https://i.imgur.com/qPtutua.png'
                        }, 
                        {
                            id: 2,
                            image: 'https://i.imgur.com/L4oTzZg.png'
                        },
                        {
                            id: 3,
                            image: 'https://i.imgur.com/gb3LEiG.png'
                        },  
                    ],
                    technologies: [
                        {
                            name: 'Vue.js',
                            img: 'https://cdn.worldvectorlogo.com/logos/vue-9.svg'
                        },
                        {
                            name: 'Quasar',
                            img: 'https://cdn.quasar.dev/logo/svg/quasar-logo.svg'
                        },
                        {
                            name: 'Vuex',
                            img: 'https://user-images.githubusercontent.com/7110136/29002857-9e802f08-7ab4-11e7-9c31-604b5d0d0c19.png'
                        }
                    ],
                    repository: null,
                    site: 'https://youpouch.netlify.app/'
                },
                {
                    id: 5,
                    name: 'Outilmaco',
                    about: 'Front-end for for fleet management system and remote monitoring for cargo trucks.',
                    images: [
                        {
                            id: 1,
                            image: 'https://i.imgur.com/z7Yhq9g.png'
                        }, 
                        {
                            id: 2,
                            image: 'https://i.imgur.com/cJPGE9k.png'
                        }, 
                    ],
                    technologies: [
                        {
                            name: 'Vue.js',
                            img: 'https://cdn.worldvectorlogo.com/logos/vue-9.svg'
                        },
                        {
                            name: 'Vuetify',
                            img: 'https://cdn.worldvectorlogo.com/logos/vuetify.svg'
                        },
                        {
                            name: 'Vuex',
                            img: 'https://user-images.githubusercontent.com/7110136/29002857-9e802f08-7ab4-11e7-9c31-604b5d0d0c19.png'
                        }
                    ],
                    repository: null,
                    site: 'https://outilmaco.netlify.app/#/'
                },
                {
                    id: 1,
                    name: 'AMano',
                    about: 'Front-end for a company that provides products, designs and architectural services plus integration with their API.',
                    images: [
                        {
                            id: 1,
                            image: 'https://i.imgur.com/Di2248H.png'
                        }, 
                        {
                            id: 2,
                            image: 'https://i.imgur.com/jcWgFpW.png'
                        }, 
                    ],
                    technologies: [
                        {
                            name: 'Vue.js',
                            img: 'https://cdn.worldvectorlogo.com/logos/vue-9.svg'
                        },
                        {
                            name: 'Quasar',
                            img: 'https://cdn.quasar.dev/logo/svg/quasar-logo.svg'
                        },
                        {
                            name: 'Vuex',
                            img: 'https://user-images.githubusercontent.com/7110136/29002857-9e802f08-7ab4-11e7-9c31-604b5d0d0c19.png'
                        }
                    ],
                    repository: null,
                    site: 'https://amanooficial.com/'
                },
                {
                    id: 2,
                    name: 'CloudProp',
                    about: 'Support for a proptech startup: rental management automation.',
                    images: [
                        {
                            id: 1,
                            image: 'https://i.imgur.com/VCGWtRz.png'
                        }, 
                        {
                            id: 2,
                            image: 'https://i.imgur.com/8OemYJM.png'
                        }, 
                    ],
                    technologies: [
                        {
                            name: 'Laravel PHP',
                            img: 'https://cdn.worldvectorlogo.com/logos/laravel-2.svg'
                        },
                        {
                            name: 'Bootstrap',
                            img: 'https://cdn.worldvectorlogo.com/logos/bootstrap-4.svg'
                        }
                    ],
                    repository: null,
                    site: 'http://www.cloudprop.com.ar/'
                },
                {
                    id: 3,
                    name: 'Cobrawi',
                    about: 'Support for massive payments notification platform.',
                    images: [
                        {
                            id: 1,
                            image: 'https://i.imgur.com/M4Ur330.png'
                        }, 
                        {
                            id: 2,
                            image: 'https://i.imgur.com/U8YKPfd.png'
                        }, 
                    ],
                    technologies: [
                        {
                            name: '.NET Core',
                            img: 'https://upload.wikimedia.org/wikipedia/commons/thumb/e/ee/.NET_Core_Logo.svg/1200px-.NET_Core_Logo.svg.png'
                        },
                        {
                            name: 'Bootstrap',
                            img: 'https://cdn.worldvectorlogo.com/logos/bootstrap-4.svg'
                        }
                    ],
                    repository: null,
                    site: 'https://www.cobrawi.com/'
                },
                {
                    id: 4,
                    name: 'Colegio de Kinesiologos del Chaco',
                    about: 'Front and backend for integral management and billing system of a professional asociation. I was part of the front end team.',
                    images: [
                        {
                            id: 1,
                            image: 'https://i.imgur.com/GVyRk4b.png'
                        }, 
                        {
                            id: 2,
                            image: 'https://i.imgur.com/qL5rEjI.png'
                        },
                        {
                            id: 3,
                            image: 'https://i.imgur.com/QTYyPUu.png'
                        }, 
                    ],
                    technologies: [
                        {
                            name: 'Asp.NET MVC5',
                            img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcT1ga1dywGmcQlQ-VSeK3GoFwQL7aAZgHj2wqM5dcbOdYCKO9T9&usqp=CAU'
                        },
                        {
                            name: 'Bootstrap',
                            img: 'https://cdn.worldvectorlogo.com/logos/bootstrap-4.svg'
                        },
                        {
                            name: 'JQuery',
                            img: 'https://cdn.worldvectorlogo.com/logos/jquery-1.svg'
                        }
                    ],
                    repository: null,
                    site: null
                },
            ],
        }
    },
    }
</script>