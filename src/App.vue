<template>
  <div>
  <v-app>

    <!-- <v-main>

      <v-card elevation="6" 
      class=" mx-auto bg-secondary rounded-lg mt-10 "
      max-width="700" >

        <v-tabs
          centered
          background-color="purple accent-4"
          dark
          next-icon="mdi-arrow-right-bold-box-outline"
          prev-icon="mdi-arrow-left-bold-box-outline"
          show-arrows>

          <v-tabs-slider color="yellow"></v-tabs-slider>

            <v-tab
              v-for="i in 4"
              :key="i"
              :href="'#tab-' + i">
              H {{ i }}
            </v-tab>
        </v-tabs>

        <v-tabs-items v-model="tabs">
          <v-tab-item>
            <v-card flat>
              <v-card-text>
                 <HelloWorld/>
              </v-card-text>
            </v-card>
          </v-tab-item>
  
          <v-tab-item>
            <v-card flat>
              <v-card-text>
                 <pesos-h-2/>
              </v-card-text>
            </v-card>
          </v-tab-item>
  
          <v-tab-item>
            <v-card flat>
              <v-card-text>
                <pesos-h-3/>
              </v-card-text>
            </v-card>
          </v-tab-item>
          <v-tab-item>
            <v-card flat>
              <v-card-text>
                <pesos-h-4/>
              </v-card-text>
            </v-card>
          </v-tab-item>
        </v-tabs-items>

      </v-card>

      

    </v-main> -->


    <v-card 
    class="mx-auto mt-10 rounded-lg"
    width="800px">

   
      <template>
        <v-tabs
          v-model="tabs"
          centered
          dark
          background-color="purple accent-4"
          show-arrows
        >
        <v-tabs-slider color="yellow lighten-1"></v-tabs-slider>
          <v-tab
            v-for="n in 4"
            :key="n"
          >
            H {{ n }}
          </v-tab>
        </v-tabs>
      </template>


      <v-tabs-items v-model="tabs">
        <v-tab-item>
          <v-card flat>
            <v-card-text>
               <HelloWorld/>
            </v-card-text>
          </v-card>
        </v-tab-item>

        <v-tab-item>
          <v-card flat>
            <v-card-text>
               <pesos-h-2/>
            </v-card-text>
          </v-card>
        </v-tab-item>

        <v-tab-item>
          <v-card flat>
            <v-card-text>
              <pesos-h-3/>
            </v-card-text>
          </v-card>
        </v-tab-item>
        <v-tab-item>
          <v-card flat>
            <v-card-text>
              <pesos-h-4/>
            </v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-card>






  </v-app>
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import PesosH2 from './components/PesosH2.vue';
import PesosH3 from './components/PesosH3.vue';
import PesosH4 from './components/PesosH4.vue';


export default {
  name: 'App',

  components: {
    HelloWorld,
    PesosH2,
    PesosH3,
    PesosH4,
},

  data () {
      return {
        tabs: null,
        text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
        tab: null,
        items: [
          { tab: 'One', content: 'Tab 1 Content' },
          { tab: 'Two', content: 'Tab 2 Content' },
          { tab: 'Three', content: 'Tab 3 Content' },
          { tab: 'Four', content: 'Tab 4 Content' },
          { tab: 'Five', content: 'Tab 5 Content' },
        ],
      }
    },
};
</script>
