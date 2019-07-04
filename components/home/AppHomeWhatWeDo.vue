<template>
  <v-container class="pa-0">
    <v-layout wrap align-center justify-center row fill-height>
      <v-layout xs12 md6 lg3 class="pa-2" justify-center="" align-center="">
        <p class="google-font" style="font-size:180%">What we do?</p>
      </v-layout>
      <v-layout row wrap>
        <v-flex xs6 sm6 md3 lg3 class="text-xs-center pa-2">
          <v-icon large style="font-size:300%">chat_bubble</v-icon>
          <p class="google-font" style="font-size:130%">Talks</p>
          <p class="google-font" style="font-size:110%">
            Get updated with the latest news and announcements
          </p>
        </v-flex>

        <v-flex xs6 sm6 md3 lg3 class="text-xs-center pa-2">
          <v-icon large style="font-size:300%">code</v-icon>
          <p class="google-font" style="font-size:130%">Codelabs</p>
          <p class="google-font" style="font-size:110%">
            Get hands-on experience and guidance from the community members
          </p>
        </v-flex>

        <v-flex xs6 sm6 md3 lg3 class="text-xs-center pa-2">
          <v-icon large style="font-size:300%">school</v-icon>
          <p class="google-font" style="font-size:130%">Campus Roadshows</p>
          <p class="google-font" style="font-size:110%">
            Share knowledge in different Companies, colleges and universities
          </p>
        </v-flex>

        <v-flex xs6 sm6 md3 lg3 class="text-xs-center pa-2">
          <v-icon large style="font-size:300%">airplay</v-icon>
          <p class="google-font" style="font-size:130%">
            Live Viewing Parties
          </p>
          <p class="google-font" style="font-size:110%">
            Share knowledge in different Companies, colleges and universities
          </p>
        </v-flex>
      </v-layout>
    </v-layout>
  </v-container>
</template>

<script>
import ChapterDetails from '~/assets/data/chapterDetails.json'
export default {
  data() {
    return {
      chapterDetails: ChapterDetails
    }
  },
  methods: {
    getImgUrl(url) {
      if (url.length > 0) {
        return `/what-we-do/${url}`
      } else {
        return '/what-we-do/notFound.png'
      }
    }
  }
}
</script>
