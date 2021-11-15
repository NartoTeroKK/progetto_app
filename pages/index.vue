<template>
  <v-container>
    <v-row 
    justify='center'>
      <v-col>
        <v-card
        class="pa-5 ma-2"
        elevation="5">
          <v-card-title>First Sprint</v-card-title>
          <v-card-text class="pt-1 ml-2">
            <p>1. Raccolta dei tweet</p>
            <p>2. Visualizzare tweet di un'emergenza</p>
            <p>3. Visualizzare tweet delle offerte di laovro</p>
          </v-card-text>
          <v-card-actions>
              <v-btn text 
              >
                User Story 1
              </v-btn>
              <v-btn text 
              >
                User Story 2
              </v-btn>
              <v-btn text 
              >
                User Story 3
              </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col>
        <v-card 
        class="pa-5 ma-2"
        elevation="5">
          prova 2
        </v-card>
      </v-col>
    </v-row>
    <v-row >
      <v-col>
        <v-card 
        class="pa-5 ma-2"
        elevation="5">
          prova 3
        </v-card>
      </v-col>
      <v-col>
        <v-card 
        class="pa-5 ma-2"
        elevation="5">
          prova 4
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import data from '../layouts/default'
export default {
  data () {
    return {
      
    }
  }
}
</script>
