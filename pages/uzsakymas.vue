<template>
  <v-content>
    <v-layout>
      <v-flex>
        <v-stepper v-model="e1">
          <v-stepper-header>
            <v-stepper-step :complete="e1 > 1" step="1"
              >Name of step 1</v-stepper-step
            >

            <v-divider></v-divider>

            <v-stepper-step :complete="e1 > 2" step="2"
              >Name of step 2</v-stepper-step
            >

            <v-divider></v-divider>

            <v-stepper-step step="3">Name of step 3</v-stepper-step>
          </v-stepper-header>

          <v-stepper-items>
            <v-stepper-content step="1">
              <v-card
                class="mb-12"
                color="grey lighten-1"
                height="200px"
              ></v-card>

              <v-btn color="primary" @click="e1 = 2">
                Continue
              </v-btn>

              <v-btn text>Cancel</v-btn>
            </v-stepper-content>

            <v-stepper-content step="2">
              <v-card
                class="mb-12"
                color="grey lighten-1"
                height="200px"
              ></v-card>

              <v-btn color="primary" @click="e1 = 3">
                Continue
              </v-btn>

              <v-btn text>Cancel</v-btn>
            </v-stepper-content>

            <v-stepper-content step="3">
              <v-card
                class="mb-12"
                color="grey lighten-1"
                height="200px"
              ></v-card>

              <v-btn color="primary" @click="e1 = 1">
                Continue
              </v-btn>

              <v-btn text>Cancel</v-btn>
            </v-stepper-content>
          </v-stepper-items>
        </v-stepper>
        <v-spacer></v-spacer>
        <h3>Vertikalus pasirinkimas</h3>
        <v-stepper v-model="e6" class="mt-4" vertical>
          <v-stepper-step :complete="e6 > 1" step="1">
            Reiki seansai
            <small>paririnkti intencija</small>
          </v-stepper-step>

          <v-stepper-content step="1">
            <v-card color="light-green darken-1" class="mb-12" height="250px">
              Kazkas apie reiki seansus cia?
              <p class="pa-2">
                Cupidatat reprehenderit sit ad et ipsum laboris magna occaecat
                duis exercitation pariatur magna duis. Qui nulla voluptate
                laboris excepteur cupidatat officia duis nisi eiusmod. Dolor
                sint et consectetur anim anim veniam esse eiusmod in ipsum
                proident qui elit. Ea veniam non veniam voluptate duis esse
                nostrud aute sit. Consequat ipsum mollit nulla veniam sit
                aliqua. Quis occaecat exercitation do sunt irure proident minim
                nisi cupidatat esse irure. Cupidatat nisi cillum sit tempor
                magna qui eiusmod do dolore qui sunt in tempor.
              </p>
            </v-card>
            <v-btn color="primary" @click="e6 = 2">Tęsti</v-btn>
            <v-btn text>Atšaukti</v-btn>
          </v-stepper-content>

          <v-stepper-step editable :complete="e6 > 2" step="2"
            >Pasirinkti intenciją</v-stepper-step
          >

          <v-stepper-content step="2">
            <v-card color="green darken-1" class="mb-12" height="250px">
              Sritys Sveikata Santykiai Sekme darbe Kita sritis... (užpildo
              žmogus pats)
            </v-card>
            <v-btn color="primary" @click="e6 = 3">Tęsti</v-btn>
            <v-btn text>Atšaukti</v-btn>
          </v-stepper-content>

          <v-stepper-step :complete="e6 > 3" step="3"
            >Select an ad format and name ad unit</v-stepper-step
          >

          <v-stepper-content step="3">
            <v-card
              color="green lighten-1"
              class="mb-12"
              height="250px"
            ></v-card>
            <v-btn color="primary" @click="e6 = 4">Tęsti</v-btn>
            <v-btn text>Atšaukti</v-btn>
          </v-stepper-content>

          <v-stepper-step step="4">View setup instructions</v-stepper-step>
          <v-stepper-content step="4">
            <v-card
              color="green lighten-2"
              class="mb-12"
              height="250px"
            ></v-card>
            <v-btn color="primary" @click="e6 = 1">Tęsti</v-btn>
            <v-btn text>Atšaukti</v-btn>
          </v-stepper-content>
        </v-stepper>
        <!-- <pre>
            Reiki seansai
                Sritys
                    Sveikata
                    Santykiai
                    Sekme darbe
                    Kita sritis... (užpildo žmogus pats)
                        Intencijos pasirinkimas (pvz geri nuoširdūs santykiai su x)

            Po intencijos pasirinkimo: 
                a) tiesiogiai
                    Miesto pasirinkimas
                        I) Vilnius
                        II) Kaunas
                        III) Klaipeda
                    <span class="yellow">Toliau kas?</span>

                b) nuotolinis
                    Meistro pasirinkimas
                        a) Meistras a
                        b) Meistas b
                    Seansu skaiciaus pasirinkimas
                        1 seansas pabandymui
                        10 seansu paketas
            
            Toliau matomas visas pasirinkimas. T.y. reziume

            Apmokejimas
        </pre> -->
      </v-flex>
    </v-layout>
  </v-content>
</template>

<script>
export default {
  data() {
    return {
      e1: 0,
      e6: 1
    }
  }
}
</script>
