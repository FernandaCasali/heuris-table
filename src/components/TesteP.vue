<template>
  <div class="text-center mt-10">
    <v-pagination
      v-model="page"
      :length="4"
      circle
    ></v-pagination>
  </div>
</template>

<script>
  export default {
    data () {
      return {
        page: 1,
      }
    },
  }
</script>