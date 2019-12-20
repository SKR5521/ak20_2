<template>
  <section id="jsf-stat">
    <v-container>
      <div v-for="(st, index) in stats" :key="index">
        <v-layout row wrap v-if="(st.year == 18)">
          <v-flex xs6 md3 class="pa-2">
            <v-layout col class="card-round elevation-6">
              <v-flex xs5 class="pa-2 flex-center">
                <v-icon class="jsf-icon">fas fa-university</v-icon>
              </v-flex>
              <v-flex xs7 class="pa-2 jsf-content">
                <h1>{{ getcollege() }}</h1>
                <h6>College</h6>
              </v-flex>
            </v-layout>
          </v-flex>
          <v-flex xs6 md3 class="pa-2">
            <v-layout col class="card-round elevation-6">
              <v-flex xs5 class="pa-2 flex-center">
                <v-icon class="jsf-icon">fas fa-map-marker-alt</v-icon>
              </v-flex>
              <v-flex xs7 class="pa-2 jsf-content">
                <h1>{{ getstate() }}</h1>
                <h6>States</h6>
              </v-flex>
            </v-layout>
          </v-flex>
          <v-flex xs6 md3 class="pa-2">
            <v-layout col class="card-round elevation-6">
              <v-flex xs5 class="pa-2 flex-center">
                <v-icon class="jsf-icon">fas fa-user-graduate</v-icon>
              </v-flex>
              <v-flex xs7 class="pa-2 jsf-content">
                <h1>{{ getstudents() }}</h1>
                <h6>Students</h6>
              </v-flex>
            </v-layout>
          </v-flex>
          <v-flex xs6 md3 class="pa-2">
            <v-layout col class="card-round elevation-6">
              <v-flex xs5 class="pa-2 flex-center">
                <v-icon class="jsf-icon">fas fa-users</v-icon>
              </v-flex>
              <v-flex xs7 class="pa-2 jsf-content">
                <h1>{{getteams()}}</h1>
                <h6>Teams</h6>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </div>
    </v-container>
  </section>
</template>

<script>
export default {
  props: ['pageid'],
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
  }),
  methods: {
    getstate() {
      console.log(this.pageid)

      return this.stats[19 - this.pageid].state
    },
    getcollege() {
      console.log(this.pageid)
      return this.stats[19 - this.pageid].college
    },
    getstudents() {
      console.log(this.pageid)
      return this.stats[19 - this.pageid].student
    },
    getteams() {
      console.log(this.pageid)
      return this.stats[19 - this.pageid].teams
    }
  }
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

  h6 {
    font-size: calc(15px + 5 * ((100vw - 320px) / 880)) !important;
    margin: 0 !important;
  }
}
.card-round {
  border-radius: 15px !important;
  background-color: aquamarine;
}
</style>