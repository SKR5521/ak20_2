<template>
  <v-footer fixed padless>
    <v-container>
      <v-layout row wrap justify-center align-content-center>
        <v-flex xs12 md6>
          <v-icon>mdi-youtube</v-icon>
          <v-icon>mdi-twitter</v-icon>
          <v-icon>mdi-facebook</v-icon>
          <v-icon>mdi-instagram</v-icon>
        </v-flex>
        <v-flex xs12 md6>//swx logo here</v-flex>
      </v-layout>
      <v-layout row wrap>
        <v-flex xs12 md6>
          <p>©2020 Dassault Systèmes SOLIDWORKS Corporation</p>
        </v-flex>
        <v-flex xs12 md6>
          <ul class="list">
            <li>
              <a href="https://www.solidworks.com/terms-use" target="_blank">Terms of Use</a>
            </li>
            <li>
              <a href="https://www.solidworks.com/privacy-policy" target="_blank">Privacy Policy</a>
            </li>
            <li>
              <a href="https://www.3ds.com/piracy/" target="_blank">Piracy Prevention</a>
            </li>
            <li>
              <a
                href="https://www.solidworks.com/license-agreement"
                target="_blank"
              >License Agreement</a>
            </li>
          </ul>
        </v-flex>
      </v-layout>
    </v-container>
  </v-footer>
</template>

<style lang="scss" >
.list {
  padding-left: 0;
  list-style: none;
}

a {
    color: $pfont;
    display: inline;
    &::hover {
        color: red;
    }
}
</style>