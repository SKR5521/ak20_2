<template>
  <div id="navbar">
    <v-toolbar color="red lighten-3">
      <v-toolbarTitle>
        <v-img :src="require('@/assets/SVGs/SW white logo.svg')"></v-img>
      </v-toolbarTitle>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn text router :to="Home.route">
          <v-icon left>{{ Home.icon}}</v-icon>
          {{Home.text}}
        </v-btn>
        <v-btn text router :to="Process.route">
          <v-icon left>{{ Process.icon}}</v-icon>
          {{Process.text}}
        </v-btn>

        <v-menu open-on-hover bottom offset-y>
          <template v-slot:activator="{on:menu}">
            <v-btn text v-on="menu">{{Oldak.text}}
              <v-icon >{{ Oldak.icon}}</v-icon>
            </v-btn>
            
          </template>
          <v-list>
            <v-list-item  v-for="item in Oldak.items" :key="item.key" router :to="item.route">
              <v-list-item-title >{{ item.text }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>

        <v-btn text router :to="faq.route">
          <v-icon left>{{ faq.icon}}</v-icon>
          {{faq.text}}
        </v-btn>
      </v-toolbar-items>
    </v-toolbar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      col: '#E31818',
      drawer: false,
      dialog: false,
      un: 3,
      updateText: [
        'Final product submission has been started. Submissions links has been emailed to all the participants.',
        'Final product submission ends on 31st August 2019.',
        'Announcing Zonal Rounds - Zonal qualifier rounds will happen in three zones Delhi, Ahmedabad and Chennai. For more details checkout Process section.'
      ],
      Home: { icon: 'fas fa-home', text: 'Home', route: '/' },
      Process: { icon: 'fas fa-cogs', text: 'Process', route: '/Process' },
      Oldak: {
        icon: 'fas fa-sort-down',
        text: 'Journey So Far',
        items: [
          { text: 'AAKRUTI2019', route: '/Previous/19' },
          { text: 'AAKRUTI2018', route: '/Previous/18' },
          { text: 'AAKRUTI2017', route: '/Previous/17' }
        ]
      },
      faq: { icon: 'fas fa-question', text: 'FAQs', route: '/faq' }
    }
  }
}
</script>

<style scoped>
.thin {
  font-family: '3ds-light';
  font-size: 34px;
}
.para {
  font-size: calc(12px + 4 * ((100vw - 320px) / 880)) !important;
}
.fontz {
  font-size: calc(14px + 2.5 * ((100vw - 320px) / 880)) !important;
  font-family: '3ds';
  margin-bottom: 12px;
  line-height: 1.2;
  letter-spacing: -0.2px;
  color: #012d52;
  /* 757575 424242*/
}
.navtogglebg {
  background: #00345c;
  background: linear-gradient(
    180deg,
    #00345c 0%,
    rgba(2, 44, 67, 0.7) 100%
  ) !important;
  font-family: '3ds';
}
.hover {
  background-color: #1e6794;
}
.display-1 {
  font-family: '3ds' !important;
}
.fontbtn {
  font-family: '3ds' !important;
  font-size: 13px !important;
}
.fontz2 {
  font-size: calc(16px + 5 * ((100vw - 320px) / 880)) !important;
  font-family: '3ds-SemiBold';
  background-color: #014a7d;
}
.v-dialog__content--active {
  background-color: rgba(0, 0, 0, 0.5) !important;
}
</style>
