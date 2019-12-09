<template>
  <section id="jsf-stat">
    <v-container>
      <v-layout row wrap>
        <v-flex xs6 md3>
          <v-card>
            <v-layout class="pa-3">
              <v-flex xs4 class="flex-center">
                <v-icon class="jsf-icon">mdi-school</v-icon>
              </v-flex>
              <v-flex class="jsf-content flex-center" xs8>
                <h1>223</h1>
                <p>Collage</p>
              </v-flex>
            </v-layout>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </section>
</template>

<style lang="scss" scoped>
.jsf-icon {
  font-size: calc(50px + 30 * ((100vw - 360px) / 880)) !important;
  color: #012d52;
  
}

.jsf-content {
  display: block;
  align-self: center;
  margin-left: 12%;
  h1 {
    font-size: calc(20px + 5 * ((100vw - 320px) / 880)) !important;
  }

  p {
    font-size: calc(15px + 5 * ((100vw - 320px) / 880)) !important;
    margin: 0 !important;
  }
}
</style>