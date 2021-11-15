<template>
  <v-app dark>
    <v-navigation-drawer
      elevation="10"
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          :to="home.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ home.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="home.title" />
          </v-list-item-content>
        </v-list-item>
        <v-list-item
          v-for="(sprint, i) in sprints"
          :key="i"
          :to="sprint.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ sprint.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="sprint.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      elevation="5"
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon v-on:click="drawer = !drawer" />
      
      <v-toolbar-title v-text="page_title" />
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      page_title: 'Twitter Web App',
      home:
        {
          title:'Home',
          icon:'mdi-home',
          to:'/'
        }
      ,
      sprints: [
        {
          id: 1,
          title: 'Sprint 1',
          sprint_goal: '',
          icon:'mdi-numeric-1-box-outline',
          to: '', //link pagina 
          user_stories: [
            {
              id: 1,
              title: 'Raccolta tweet',
              info: 'Come acquirente di un ticket per un evento voglio poter visualizzare l\'hashtag di tale evento, per poter essere aggiornato su nuove attività o cambi di programma',
              to: 'sprint1_us1'
            },
            {
              id: 2,
              title: 'Visualizzazione tweet offerte di lavoro',
              info: 'Come utente voglio poter visualizzare i tweet relativi alle offerte di lavoro in una determinata zona per valutare eventuali nuove opportunità lavorative',
              to: 'sprint1_us2'
            },
            {
              id: 3,
              title: 'Visualizzazione tweet emergenza',
              info: 'Come utente voglio visualizzare tweet relativi alle ultime emergenze in Italia per poter rimanere in allerta',
              to: 'sprint1_us3'
            }
          ]
        }
      ]
    }
  }
}
</script>
