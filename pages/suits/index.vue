<template>
  <v-layout
    ><v-container class="grey lighten-5 mt-5 mb-5">
      <p class="display-1 grey--text text--darken-4 font-weight-black">
        現在の訴訟準備中一覧
      </p>
      <suits-ready /> </v-container
  ></v-layout>
</template>

<script>
import SuitsReady from '~/components/SuitsReady'
export default {
  components: { SuitsReady },
  computed: {}
}
</script>
