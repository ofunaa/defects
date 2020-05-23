<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <v-card>
        <v-card-title class="headline">
          （DEMO）SNSの誹謗中傷を簡単に訴訟することができるクラウドファンディング
        </v-card-title>
        <v-card-text>
          <ul>
            <li>誹謗中傷は犯罪です</li>
            <li>
              しかし、その犯罪行為を訴訟する。ということが日本ではまだ主流ではありません
            </li>
            <li>
              どうせ訴えられないだろう。という軽い気持ちで誹謗中傷を行う人が多くいます
            </li>
            <li>
              その人たちを止めるには、たった一言でも訴えられるんだ。とリスクを提示する必要があります
            </li>
            <br />
            <li>
              現在、誹謗中傷が訴訟されない理由としては、以下のようなことがあげられると思います
            </li>
            <ul>
              <li>訴訟の方法がわからない</li>
              <li>訴訟の費用負担が厳しい</li>
              <li>時間がかかりそう</li>
              <li>...etc</li>
            </ul>
            <br />
            <li>
              その問題を全て解決するのが、訴訟クラウドファンディングのdefectsです
            </li>
            <li>
              defects での作業は以下の通りです
            </li>
            <ul>
              <li>
                誹謗中傷のスクリーンショット・魚拓を掲載し、訴訟費用を募集します
              </li>
              <li>
                SNS 等で拡散します
              </li>
              <li>
                訴訟費用が集まり次第、提携している弁護士を通じて、訴訟を行います
              </li>
            </ul>
          </ul>
        </v-card-text>
      </v-card>
    </v-flex>
    <v-container class="grey lighten-5 mt-5 mb-5">
      <p class="display-1 grey--text text--darken-4 font-weight-black">
        現在の訴訟準備中一覧
      </p>
      <suits-ready />
    </v-container>
  </v-layout>
</template>

<script>
import SuitsReady from '~/components/SuitsReady'
export default {
  components: { SuitsReady },
  computed: {}
}
</script>
