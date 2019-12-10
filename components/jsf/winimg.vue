<template>
  <section id="winImages">
    <v-layout row wrap>
      <v-flex xs12 md6 >
        <v-card class="divclass flex-center">
          <h1>This is a test card</h1>
        </v-card>
      </v-flex>
      <v-flex xs12 md6 >
        <v-card class="divclass flex-center">
          <h1>This is a test card</h1>
        </v-card>
      </v-flex>
    </v-layout>
  </section>
</template>

<style lang="scss" scoped>
.divclass {
  width: 90%;
  height: 300px;
  margin: 2% auto;

  background-image: url('https://cdn.vuetifyjs.com/images/cards/docks.jpg');
  border-radius: 15px !important;
}
</style>