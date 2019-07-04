<template>
  <v-container class="pa-0">
    <v-layout wrap align-center justify-center row fill-height>
      <v-flex xs12 sm5 md3 lg3 xl3 class="text-xs-center pa-3">
        <v-img src="gdg.jpg" lazy-src="gdg.jpg" width="100%">
          <v-layout>
            <v-progress-circular />
          </v-layout>
        </v-img>
      </v-flex>
      <v-flex xs12 sm7 md8 lg8 xl8 class="">
        <p
          class="google-font mb-1"
          style="font-weight: 350;color: #616161;font-size:300%"
        >
          <b>Make good things <span style="color: #1a73e8;">together</span>.</b>
        </p>
        <p class="google-font" style="font-size:110%">
          {{ chapterDetails.ChapterShortDescription }}
        </p>
        <p class="google-font" style="font-size:110%;color:#9e9e9e">
          <span v-for="(item, i) in chapterDetails.ChapterHashTags" :key="i">
            #{{ item }} &nbsp;
          </span>
        </p>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import ChapterDetails from '~/assets/data/chapterDetails'

export default {
  data() {
    return {
      chapterDetails: ChapterDetails
    }
  }
}
</script>

<style></style>
