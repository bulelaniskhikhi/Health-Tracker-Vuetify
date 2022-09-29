<template>
  <v-app :style="{background: $vuetify.theme.themes.light.background}">
    <v-layout row>
      <v-flex md8>
        <v-app :style="{background: $vuetify.theme.themes.dark.background}" class="rounded-tr-xl rounded-br-xl">
          <v-container>
            <v-row>
              <v-col cols="12" sm="12">
                <v-app-bar color="rgba(0,0,0,0)" flat class="mx8 mb-8 mt-3">
                  <v-text-field
                  prepend-icon="mdi-magnify"
                  color="black"
                  placeholder="Search your syptoms"
                  flat       
                  >
                  
                  </v-text-field>
                  <v-spacer></v-spacer>
                  <v-chip class="ma-2" color="white">
                    <v-icon left color=black>
                      mdi-clock-time-nine
                    </v-icon>
                    14:12 AM Today Nov,19
                  </v-chip>
                </v-app-bar>
              </v-col>
              <v-col cols="12" sm="12">
                <v-card class="mx-12 rounded-tl-xl rounded-tr-xl rounded-bl-xl rounded-br-xl mt-n15">
                  <v-list-item three-line>
                    <v-list-item-content class="pa-10">
                      <v-list-item-title class="headline mb-1">
                        today <span style="color: #757575">-10%</span> discount<br/>
                        on lung examinations 
                      </v-list-item-title>
                      <v-list-item-subtitle>
                        The package price includeds: consultation<br/>
                        of a pulmonologist, spirography, cardigram <span class="teal--text"></span>
                      </v-list-item-subtitle>
                    </v-list-item-content>
                    <v-list-item-content>
                      <v-list-item-avatar tile size="150" class="pr-10">

                        <img src="lungs.jpg">
                      </v-list-item-avatar>
                    </v-list-item-content>
                  </v-list-item>
                </v-card>
              </v-col>
              <v-col cols="12" sm="12">
                <v-card class="mx-12" rounded-tl-xl rounded-tr-xl rounded-bl-xl rounded-br-xl mt-n10>
                  <v-app-bar color="rgba(0,0,0,0)" flat class="ma-8">
                    <h5>Statistics of your health</h5>
                    <v-spacer></v-spacer>
                    <v-btn color="black" text>
                      2019
                      <v-icon right>mdi-chevron-down</v-icon>
                    </v-btn>
                    <v-btn color="black" rounded dark depressed>
                      Year
                    </v-btn>
                    <v-btn text>Mounth</v-btn>
                  </v-app-bar>
                  <template>
                    <v-sparkline 
                    :value="value"
                    color="black"
                    :smooth="radius || false"
                    :padding="padding"
                    :line-width="width"
                    :stroke-linecap="linecap"
                    :fill="fill"
                    :type="type"
                    :auto-line-width="autoLineWidth"
                    auto-draw
                    >

                    </v-sparkline>
                  </template>
                </v-card>
              </v-col>
              <v-col cols="12" sm="6">
                <v-card class="mx-12 rounded-tl-xl rounded-tr-xl rounded-bl-xl rounded-br-xl mt-n4" color="black">
                  <v-list-item three-line>
                    <v-list-item-content class="pa-2">
                      <v-list-item-content class="pa-2">
                        <v-list-item-title style="color: white" class="headline md-1">
                          Heart rate <br/>
                          <h2>112 bpm</h2>
                        </v-list-item-title>
                      </v-list-item-content>
                      <v-list-avatar  tile size="150" class="pr-10">
                        <v-icon style="color: white" size="100">
                          fas fa-heartbeat
                        </v-icon>
                      </v-list-avatar>
                    </v-list-item-content>
                  </v-list-item>
                </v-card>
              </v-col>
              <v-col cols="12" sm="6">
                <v-card class="mx-12 rounded-tl-xl rounded-tr-xl rounded-bl-xl rounded-br-xl mt-n12">
                  <v-app-bar color="rgba(0,0,0,0)" flat class="ma-8">
                    <h5>Your activity</h5>
                    <v-spacer></v-spacer>
                    <v-btn color="black" rounded dark depressed>Week</v-btn>
                    <v-btn text>Mounth</v-btn>
                  </v-app-bar>
                  <v-progress-circular rotate="360" size="100" width="15" value="50" color="#757575" class="mt-n5 ml-5 mb-2">
                   50
                  </v-progress-circular>
                  <v-progress-circular rotate="360" size="100" width="15" value="70" color="#424242" class="mt-n5 ml-5 mb-2">
                   70
                  </v-progress-circular>
                  <v-progress-circular rotate="360" size="100" width="15" value="90" color="grey darken-4" class="mt-n5 ml-5 mb-2">
                   90
                  </v-progress-circular>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-app>
      </v-flex>
      <v-flex md4>
        <v-app :style="{background: $vuetify.theme.themes.light.background}">
          <v-container>
            <v-row>
              <v-col cols="12" sm="12">
                <v-list two-line>
                  <v-list-item>
                    <v-list-item-avater>
                      <img scr="http://cdn.vuetifyjs.com/images/list/3.jpg"></img>
                    </v-list-item-avater>
                    <v-list-item-content>
                      <v-list-item-title>
                        Anastasia Turner
                      </v-list-item-title>
                      <v-list-item-subtitle class="black--text">
                        37 years, California
                      </v-list-item-subtitle>
                    </v-list-item-content>
                    <v-space></v-space>
                    <v-icon color="black">
                      mdi-menu
                    </v-icon>
                  </v-list-item>
                </v-list>
              </v-col>

              <v-col cols="12" md="4">
                <v-row>
                  <v-col cols="12" md="2">
                    <v-card height="50px" width="10px" color="black">
                    </v-card>
                  </v-col>
                  <v-col cols="12" md="10" >
                    <v-list two-line subheader class="ml-n8">
                      <v-list-item>
                        <v-list-item-content>
                          <v-list-item-subtitle>
                            Blood
                          </v-list-item-subtitle>
                          <v-list-item-title>
                            O-
                          </v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-list>
                  </v-col>
                </v-row>
              </v-col>

              <v-col cols="12" md="4">
                <v-row>

                  <v-col cols="12" md="2">
                    <v-card height="50px" width="10px" color="black">
                    </v-card>
                  </v-col>

                  <v-col cols="12" md="10" >
                    <v-list two-line subheader class="ml-n8">
                      <v-list-item>
                        <v-list-item-content>
                          <v-list-item-subtitle>
                            Height
                          </v-list-item-subtitle>
                          <v-list-item-title>
                            165 cm
                          </v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-list>
                  </v-col>

                 </v-row>
              </v-col>

              <v-col cols="12" md="4">
                <v-row>
                  <v-col cols="12" md="2">
                    <v-card height="50px" width="10px" color="black">
                    </v-card>
                  </v-col>

                  <v-col cols="12" md="10" >
                    <v-list two-line subheader class="ml-n8">
                      <v-list-item>
                        <v-list-item-content>
                          <v-list-item-subtitle>
                            Weight
                          </v-list-item-subtitle>
                          <v-list-item-title>
                            65 KG
                          </v-list-item-title>
                        </v-list-item-content>
                      </v-list-item>
                    </v-list>
                  </v-col>

                </v-row>
              </v-col>
              <v-col cols="12" sm="12">
                <v-btn text>
                  November
                  <v-icon right>
                    mdi-chevron-down
                  </v-icon>
                </v-btn>
              </v-col>
              <v-col cols="12" sm="12" >
                <v-list-item>
                  <v-list-item-content>
                    <v-btn style="color: white" class="mr-1" outline color="black">
                      Mon
                    </v-btn>
                  </v-list-item-content>
                  <v-list-item-content>
                    <v-btn style="color: white" class="mr-1" outline color="black">
                      Tue
                    </v-btn>
                  </v-list-item-content>
                  <v-list-item-content>
                    <v-btn style="color: white" class="mr-1" outline color="black">
                      Wed
                    </v-btn>
                  </v-list-item-content>
                  <v-list-item-content>
                    <v-btn style="color: white" class="mr-1" outline color="black">
                      Thu
                    </v-btn>
                  </v-list-item-content>
                  <v-list-item-content>
                    <v-btn style="color: white" class="mr-1" outline color="black">
                      Fri
                    </v-btn>
                  </v-list-item-content>
                  <v-list-item-content>
                    <v-btn style="color: white" class="mr-1" outline color="black">
                      Sat
                    </v-btn>
                  </v-list-item-content>
                  <v-list-item-content>
                    <v-btn style="color: white" class="mr-1" outline color="black">
                      Sun
                    </v-btn>
                  </v-list-item-content>
                </v-list-item>
              </v-col>
              <v-col cols="12" sm="12">
                <v-card class="mx-12 rounded-tl-xl rounded-tr-xl rounded-br-xl rounded-bl-xl mt-n4 py-4" 
                color="black" dark flat>
                  <v-list-item three-line>
                    <v-list-item-avatar tile size="30">
                      <v-icon size="30">
                        mdi-tooth
                      </v-icon>
                    </v-list-item-avatar>
                    <v-list-item-content class="pa-2">
                      <v-list-item-title class="headeline md-1">
                        Dentist <br/>
                        <h6>8:00 - 9:30</h6>
                        <h6>Dr. Benjamin Reichwald</h6>
                      </v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-card>
              </v-col>

              <v-col cols="12" sm="12">
                <v-card class="mx-12 rounded-tl-xl rounded-tr-xl rounded-bl-xl rounded-br-xl m-n4 py-4"
                color="grey darken-3" dark flat>
                  <v-list-item three-line>
                    <v-list-item-avatar tile size="30">
                      <v-icon style="color: white" size="30">
                        fas fa-heartbeat
                      </v-icon>
                    </v-list-item-avatar>
                    <v-list-item-content class="pa-2">
                      <v-list-item-title class="headeline md-1">
                        Cardiologist <br/>
                        <h6>9:45 - 11:50</h6>
                        <h6>Dr. Zak Arogundade Gaterud</h6>
                      </v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-card>
              </v-col>

              <v-list cols="12" sm="12" class="mx-12">
                <v-btn text>
                 Your Traitment
                 <v-icon right>
                  mdi-chevron-down
                 </v-icon>
                </v-btn>
              </v-list>

              <v-col cols="12" sm="12">
                  <v-card class="mx-12 rounded-tl-xl rounded-tr-xl rounded-br-xl rounded-bl-xl mt-n4"
                  color="grey lighten-2" flat>
                    <v-list-item three-line>
                      <v-list-item-avatar tile size="30">
                        <v-icon size="30" color="black">
                          mdi-pill
                        </v-icon>
                      </v-list-item-avatar>
                      <v-list-item-content class="pa-2">
                        <v-list-item-title class="headline mb-1">
                          Gentle iron<br/>
                          <h6><span class="gray--text">2 capsules</span></h6>
                        </v-list-item-title>
                      </v-list-item-content>
                    </v-list-item>
                  </v-card>
                </v-col>
            </v-row>
          </v-container>
        </v-app>
      </v-flex>
    </v-layout>
  </v-app>
</template>

<script>
  
  export default {
    data: () => ({
      width:2,
      radius: 10,
      padding: 8,
      lineCap: 'round',
      value: [0,3,7,2,5,6,7,8,5,2],
      fill: false,
      type: 'trend',
      autoLineWidth: false
    }),
    computed: {
      theme() {
        return this.$vuetify.theme.dark ? "dark" : "light";
      }
    }
  }
</script>
