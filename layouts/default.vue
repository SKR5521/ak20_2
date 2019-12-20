<template>
  <v-app class="bdy">
     <Navbar/>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <foot />
  </v-app>
</template>

<script>
import foot from '@/components/foot'
import Navbar from '@/components/Navbar'

export default {
  components: {
    foot,
    Navbar
  },
  data() {
    return {
      //
    }
  }
}
</script>

<style lang="scss">
.bdy {
  margin: 0;
  padding: 0;
  background-color: $bg !important;
  font-size: 14px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.tb {
  @extend .bdy;

  color: yellow;
}
</style>