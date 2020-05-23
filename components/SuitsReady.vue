<template>
  <v-row no-gutters>
    <v-col v-for="n in 6" :key="n" cols="12" sm="4">
      <v-card class="ma-1 pa-1 mb-4" outlined tile>
        <v-card-text>
          <div>{{ today }}</div>
          <p class="headline text--primary">
            DEMO）SNSの誹謗中傷を訴訟します
          </p>
          <div class="text--primary">
            毎日毎日、誹謗中傷を投げかけてくる人がいます
          </div>
          <p class="mt-5">目標に対する達成率</p>
          <v-progress-linear
            class="mb-1"
            value="76"
            height="10"
          ></v-progress-linear>
        </v-card-text>
        <v-card-actions>
          <v-btn depressed large color="error" href="suits/1">応援する</v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  computed: {
    today() {
      const nowDate = new Date()

      const year = nowDate.getFullYear()
      const month = nowDate.getMonth() + 1
      const day = nowDate.getDate()

      return year + '/' + month + '/' + day
    }
  }
}
</script>
