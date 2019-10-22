<template>
  <v-app>
    <v-container fill-height>
      <v-row justify="center" align="center">
        <v-col cols="12" class="text-center">
         <h1 class="display-4">Jonathan Gomez's Portfolio</h1>
        </v-col>
        <v-col cols="12" class="text-center display-1">
          <p>Johnnygoez@hotmail.com</p>
        </v-col>
        <v-col>
            <v-container>
              <v-row justify="center">
                <v-col cols="4" v-for="(project, index) in projects" :key="index">
                     <v-card
    max-width="344"
    class="mx-auto"
  >
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title class="headline">{{project.name}}</v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-img
      :src="project.screenshot" contain
      height="194"
    ></v-img>

    <v-card-text>
      {{project.description}}
    </v-card-text>

    <v-card-actions>
      <v-btn
        text
        color="blue accent-4" :href="project.url" target="_blank">
        Go to site
      </v-btn>
      <div class="flex-grow-1"></div>
      <v-btn icon>
        <v-icon>mdi-share-variant</v-icon>
      </v-btn>
    </v-card-actions>
  </v-card>
                </v-col>
          </v-row>
        </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    projects: [
      {
        name: 'Vue Todo Application',
        description: 'A simple to do application wwho handles completed and pending tasks, it also keeps record of total tasks per bucket.',
        screenshot: '/images/vue-todo.png',
        url: 'https://todo.jonathan-gomez.site'
      },
      {
        name: 'Marvel Finder',
        description: 'Using Marvel Public API, we have a simple character finder application, with character description and also some comics in which they appear in.',
        screenshot: '/images/marvelfinder.png',
        url: 'https://marvelfinder.jonathan-gomez.site'
      },
      {
        name: 'Super Awesome App',
        description: 'The coolest and best social network app ever created.',
        screenshot: '/images/super-awesome-app.png',
        url: 'https://superawesomeapp.jonathan-gomez.site'
      }
    ]
  })
}
</script>
