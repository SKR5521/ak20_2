<template>
  <div id="winImages">
    <v-container >
      <v-layout row wrap>
      <v-flex xs12 md6 >
        <v-card :class="sameclass">          
          <v-img :src="require('@/assets/imgs/PreviousYear/19/1.png')" aspect-ratio="1"></v-img>
        </v-card>
      </v-flex>
      <v-flex xs12 md6 >
        <v-card :class="sameclass">
           <v-img  :src="require('@/assets/imgs/PreviousYear/19/2.png')" aspect-ratio="1"></v-img>
        </v-card>
      </v-flex>
      <v-flex xs12 md6 >
        <v-card :class="sameclass">          
          <v-img :src="require('@/assets/imgs/PreviousYear/19/3.png')" aspect-ratio="1"></v-img>
        </v-card>
      </v-flex>
      <v-flex xs12 md6 >
        <v-card :class="sameclass">
           <v-img  :src="require('@/assets/imgs/PreviousYear/19/4.png')" aspect-ratio="1"></v-img>
        </v-card>
      </v-flex>
    </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return({
      sameclass: 'divclass ma-3 flex-center'
    })
  }
}
</script>

<style lang="scss" scoped>
#divclass {
  width: 90%;
  height: 400px;

  border-radius: 15px !important;
}
</style>