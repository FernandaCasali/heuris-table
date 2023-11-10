<template>
  <div>


  <v-app>
    <v-card 
    class=" mx-auto bg-secondary rounded-lg mt-10 "
    :class="`elevation-${14}`"
    max-width="600" >

    <div class="text-center">

      <v-pagination
      v-model="page"
      :length="4"
      circle
      color="purple accent-4"
      >
    
      </v-pagination>

    </div>

  </v-card>

    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</div>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data () {
      return {
        page: 1,
      }
    },
};
</script>
