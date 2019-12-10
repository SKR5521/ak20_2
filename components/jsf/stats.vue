<template>
  <section id="jsf-stat">
    <v-container v-for="(st, index) in stats" :key="index">
      <v-layout row wrap v-if="(st.year == 18)">
        <v-flex xs6 md3 class="pa-2">
          <v-card class="card-round elevation-5 mx-2">
            <v-layout col>
              <v-flex xs4 class="flex-center">
                <v-icon class="jsf-icon">fas fa-university</v-icon>
              </v-flex>
              <v-flex class="jsf-content flex-center pl-3" xs8>
                <h1>{{ st.college }}</h1>
                <p>College</p>
              </v-flex>
            </v-layout>
          </v-card>
        </v-flex>
        <v-flex xs6 md3 class="pa-2">
          <v-card class="card-round elevation-5 mx-2">
            <v-layout col>
              <v-flex xs4 class="flex-center">
                <v-icon class="jsf-icon">fas fa-map-marker-alt</v-icon>
              </v-flex>
              <v-flex class="jsf-content flex-center pl-3" xs8>
                <h1>{{ st.state }}</h1>
                <p>States</p>
              </v-flex>
            </v-layout>
          </v-card>
        </v-flex>
        <v-flex xs6 md3 class="pa-2">
          <v-card class="card-round elevation-5 mx-2">
            <v-layout col>
              <v-flex xs4 class="flex-center">
                <v-icon class="jsf-icon">fas fa-user-graduate</v-icon>
              </v-flex>
              <v-flex class="jsf-content flex-center pl-3" xs8>
                <h1>{{ st.student }}</h1>
                <p>Students</p>
              </v-flex>
            </v-layout>
          </v-card>
        </v-flex>
        <v-flex xs6 md3 class="pa-2">
          <v-card class="card-round elevation-5 mx-2">
            <v-layout col>
              <v-flex xs4 class="flex-center">
                <v-icon class="jsf-icon">fas fa-users</v-icon>
              </v-flex>
              <v-flex class="jsf-content flex-center pl-3" xs8>
                <h1>{{ st.teams }}</h1>
                <p>Teams</p>
              </v-flex>
            </v-layout>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </section>
</template>

<script>
export default {
  data: () => ({
    stats: [
      {
        year: '19',
        student: '4932',
        state: '26',
        college: '332',
        teams: '2466'
      },
      {
        year: '18',
        student: '2240',
        state: '24',
        college: '218',
        teams: '1120'
      },
      {
        year: '17',
        student: '1700',
        state: '21',
        college: '196',
        teams: '850'
      },
      {
        year: '16',
        student: '1632',
        state: '19',
        college: '146',
        teams: '816'
      }
    ]
  })
}
</script>

<style lang="scss" scoped>
.jsf-icon {
  font-size: calc(40px + 8 * ((100vw - 360px) / 880)) !important;
  color: #012d52;
}

.jsf-content {
  display: block;
  align-items: center;
  h1 {
    font-size: calc(20px + 5 * ((100vw - 320px) / 880)) !important;
  }

  p {
    font-size: calc(15px + 5 * ((100vw - 320px) / 880)) !important;
    margin: 0 !important;
  }
}
.card-round {
  border-radius: 15px !important;
}
</style>