<template>
  <v-footer color="white" height="auto" class="hidden-sm-and-down">
    <v-container
      fluid
      style="border-color:#e0e0e0;border-width: 1px;border-style: solid;border-bottom: 0"
    >
      <v-layout wrap justify-center row>
        <v-flex xs12 md10 lg10>
          <v-layout wrap align-start justify-start row class="my-2">
            <v-flex xs12 md3 sm4 lg3 class="py-2">
              <p
                class="google-font mb-0"
                style="font-size: 140%;font-weight: 300;"
              >
                <b>About</b>
              </p>
              <div
                v-for="(item, i) in FooterData.AboutSession"
                :key="i"
                class="mt-1"
              >
                <a
                  :href="item.Link"
                  class="google-font"
                  target="_blank"
                  style="color: #3E4551;text-decoration: none;font-size:110%"
                >
                  {{ item.LinkName }}
                </a>
                <br />
              </div>
            </v-flex>

            <v-flex xs12 md3 sm4 lg3 class="py-2">
              <p
                class="google-font mb-0"
                style="font-size: 140%;font-weight: 300;"
              >
                <b>Resources</b>
              </p>
              <div
                v-for="(item, i) in FooterData.ChapterResourcesSession"
                :key="i"
                class="mt-1"
              >
                <a
                  :href="item.Link"
                  class="google-font"
                  target="_blank"
                  style="color: #3E4551;text-decoration: none;font-size:110%"
                >
                  {{ item.LinkName }}
                </a>
                <br />
              </div>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>

      <v-layout wrap justify-center row class="mb-0">
        <v-flex xs12 md10 lg10>
          <v-divider></v-divider>
          <v-toolbar
            flat
            color="white"
            class="pa-0 mx-0"
            style="padding:0 !important"
          >
            <v-toolbar-title
              class="google-font pl-0 ml-0 mr-3"
              style="font-size:200%"
              >{{ ChapterDetails.ChapterName }}</v-toolbar-title
            >
          </v-toolbar>
        </v-flex>
      </v-layout>
    </v-container>
  </v-footer>
</template>

<script>
import ChapterDetails from '~/assets/data/chapterDetails.json'
import FooterData from '~/assets/data/footer.json'
export default {
  data() {
    return {
      ChapterDetails: ChapterDetails,
      FooterData: FooterData
    }
  }
}
</script>
