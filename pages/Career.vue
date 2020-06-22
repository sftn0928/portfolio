
<template>
  <div class="career-wrapper">
    <Title title="Career" id="Career" />
    <div class="fade-in-el" v-scroll-inview:fadeIn>
      <v-timeline>
        <v-timeline-item
          v-for="(career, index) in careers"
          :key="index"
          color="blue lighten-2"
          large
        >
          <template v-slot:opposite>
            <span>{{ career.ym }}</span>
          </template>
          <v-card class="elevation-2">
            <v-card-title class="primary">{{ career.title }}</v-card-title>
            <v-card-text>
              {{ career.content }}
            </v-card-text>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </div>
  </div>
</template>

<script>
import Title from "@/components/Title.vue";
export default {
  components: {
    Title
  },
  data() {
    return {
      fadeInOption: {
        delay: 2
      },
      careers: [
        { ym: "2018/4", title: "大学（工学部 情報系）に入学" },
        { ym: "2019/5", title: "基本情報技術者試験 合格" },
        { ym: "2019/8", title: "学生エンジニア団体 steg 加入" },
        { ym: "2020/2", title: "Web制作（初案件）をこなす" },
        { ym: "2020/4", title: "企業主催のハッカソンに出場" }
      ]
    };
  }
};
</script>

<style></style>
