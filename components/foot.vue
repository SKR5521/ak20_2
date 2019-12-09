<template>
  <v-footer fixed padless class="flex-center pa-2">
    <div class="container">
      <v-layout row wrap class="pb-4">
        <v-flex xs12 md6 class="flex-center py-3">
          <v-btn
            v-for="item in items"
            :key="item.icon"
            class="mx-3 px-auto"
            target="_blank"
            fab
            :href="item.ref"
          >
            <v-icon>{{ item.icon }}</v-icon>
          </v-btn>
        </v-flex>
        <v-flex xs12 md6 class="flex-center py-auto">
          <v-img
            contain
            max-height="45px"
            class="my-auto"
            :src="require('../assets/SVGs/SW red logo.svg')"
            alt="SW red logo"
          ></v-img>
        </v-flex>
      </v-layout>

      <v-divider></v-divider>

      <v-layout row wrap class="pt-4">
        <v-flex xs12 md6 class="pt-3 flex-center">
          <p class="px-2 ma-0">©2020 Dassault Systèmes SOLIDWORKS Corporation</p>
        </v-flex>
        <v-flex xs12 md6 class="py-3 flex-center">
          <div id="foot-links" class="text-xs-center">
            <a class="pr-2" href="https://www.solidworks.com/terms-use" target="_blank">Terms of Use</a>
            <a
              class="pr-2"
              href="https://www.solidworks.com/privacy-policy"
              target="_blank"
            >Privacy Policy</a>
            <a class="pr-2" href="https://www.3ds.com/piracy/" target="_blank">Piracy Prevention</a>
            <a
              class="pr-2"
              href="https://www.solidworks.com/license-agreement"
              target="_blank"
            >License Agreement</a>
          </div>
        </v-flex>
      </v-layout>
    </div>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        icon: 'mdi-facebook',
        ref: 'https://www.facebook.com/AakrutiContest/'
      },
      {
        icon: 'mdi-linkedin',
        ref: 'https://www.linkedin.com/showcase/solidworks/'
      },
      {
        icon: 'mdi-twitter',
        ref: 'https://twitter.com/solidworks'
      },
      {
        icon: 'mdi-youtube',
        ref: 'https://www.youtube.com/solidworks'
      }
    ]
  })
}
</script>

<style lang="scss" scoped>
a {
  color: $bg !important;
  font-family: 'ds';
  text-decoration: none;
  font-size: calc(14px + 4 * ((100vw - 360px) / 880)) !important;

  &:hover {
    color: purple !important;
  }
}

#foot-links {
  @extend a;
  display: inline;
}
</style>