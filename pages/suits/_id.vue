<template>
  <v-layout>
    <v-flex>
      <v-card class="pa-4 ma-4">
        <p class="headline">DEMO）SNSの誹謗中傷を訴訟します</p>
        <p>申請日: {{ today }}</p>
        <a
          href="https://twitter.com/share?ref_src=twsrc%5Etfw"
          class="twitter-share-button"
          data-show-count="false"
          >Tweet</a
        >
        <script
          async
          src="https://platform.twitter.com/widgets.js"
          charset="utf-8"
        ></script>

        <p class="font-weight-black mt-10">■ 該当のスクリーンショット</p>
        <p>※本番では、アカウント名などもぼかさずにスクショを載せます</p>
        <v-img
          :src="require('@/assets/waruguchi.jpg')"
          height="125"
          class="grey darken-4"
        ></v-img>

        <p class="font-weight-black mt-10">■ 該当のWEB魚拓 URL</p>
        <p><a href="https://megalodon.jp/">https://megalodon.jp/</a></p>

        <p class="font-weight-black mt-10">■ 訴訟者からのコメント</p>
        <p>毎日毎日、誹謗中傷を浴びせられています。助けてください。</p>
        <p></p>

        <p class="font-weight-black mt-10">■ 目標進捗</p>
        <p>375,000 / 500,000円</p>
        <v-progress-linear
          class="mb-1"
          value="75"
          height="30"
        ></v-progress-linear>

        <v-card-actions class="mt-10">
          <v-dialog v-model="dialog" scrollable max-width="500px">
            <template v-slot:activator="{ on }">
              <v-btn color="error" dark v-on="on">応援する</v-btn>
            </template>
            <v-card>
              <v-card-title>募金額を決める</v-card-title>
              <v-divider></v-divider>
              <v-card-text style="height: 300px;">
                <v-radio-group v-model="dialogm1" column>
                  <v-radio label="500円" value="500"></v-radio>
                  <v-radio label="1,000円" value="1000"></v-radio>
                  <v-radio label="5,000円" value="5000"></v-radio>
                  <v-radio label="10,000円" value="10000"></v-radio>
                  <v-radio label="50,000円" value="50000"></v-radio>
                </v-radio-group>
              </v-card-text>
              <p>※ デモなので実際に課金されることはありません</p>
              <v-divider></v-divider>
              <v-card-actions>
                <v-btn color="blue darken-1" text @click="bokin"
                  >募金する</v-btn
                >
                <v-btn color="blue darken-1" text @click="dialog = false"
                  >募金しない</v-btn
                >
              </v-card-actions>
            </v-card>
          </v-dialog>
        </v-card-actions>
      </v-card>
    </v-flex>
    <v-snackbar v-model="snackbar" :timeout="timeout">
      {{ text }}
      <v-btn color="blue" text @click="snackbar = false">
        Close
      </v-btn>
    </v-snackbar>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      dialogm1: '',
      dialog: false,
      snackbar: false,
      text: 'DEMOなので課金はされません）募金完了しました。',
      timeout: 10000
    }
  },
  methods: {
    bokin() {
      this.dialog = false
      this.snackbar = true
    }
  },
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
