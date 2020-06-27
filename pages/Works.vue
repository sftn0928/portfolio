<template>
  <div clss="works-wrapper">
    <Title title="Works" id="Works" />

    <div class="works-content">
      <WorkBox :items="contents" />
    </div>
  </div>
</template>

<script>
import Title from "@/components/Title";
import WorkBox from "@/components/WorkBox";
export default {
  components: {
    Title,
    WorkBox
  },
  data() {
    return {
      contents: [
        {
          imgUrl: require("~/assets/images/portfolio.png"),
          title: "portfolio",
          sentence: "私の自己紹介サイトです。Nuxt.js＋Vuetifyで作成しました。",
          workUrl: "https://sftn0928.netlify.com"
        },
        {
          imgUrl: require("~/assets/images/fablechord.png"),
          title: "FableChord",
          sentence: "初めて担当したWeb制作案件です。デザインは外部に委託しました。",
          workUrl: "http://fablechord.com/"
        },
        {
          imgUrl: require("~/assets/images/YouTubeLiveApp.png"),
          title: "YouTubeライブアンケート(6月中にデプロイ予定）",
          sentence:
            "YouTubeの生放送中にコメントを集計して、アンケートを実施するアプリです。Nuxt.js＋Expressで作成。３人１組のハッカソンで作成しました。私は主にフロントエンドを担当して、少しだけバックも書きました。",
          workUrl: ""
        },
        {
          imgUrl: require("~/assets/images/admireApp.png"),
          title: "メッセージ称賛アプリ(未デプロイ)",
          sentence:
            "React.jsで作成した某企業のインターン課題です。簡易的なSNS？のようなもの。インターンの選考が通ったら、ブラッシュアップ予定。許可を得ていないのでデプロイはしません。",
          workUrl: ""
        },
        {
          imgUrl: require("~/assets/images/TDU-calculationApp.png"),
          title: "TDU単位計算アプリ(作成中)",
          sentence:
            "私が通っている大学の単位計算サイトです。新規登録をすれば誰でも使えます。（EC科のみ）Nuxt.js＋Expressで作成中。",
          workUrl: ""
        }
        // {
        //   imgUrl: require(""),
        //   title: "",
        //   sentence: "",
        //   workUrl: ""
        // }
      ]
    };
  }
};
</script>

<style></style>
