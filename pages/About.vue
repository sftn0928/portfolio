<template>
  <div class="about-wrapper">
    <Title title="About" id="About" />
    <div class="fade-in-el" v-scroll-inview:fadeIn>
      <v-card class="about-content">
        <div></div>
        <v-avatar size="300" class="my-3">
          <img
            class="profile-img"
            src="~/assets/images/profile.jpg"
            alt="プロフィール画像"
          />
        </v-avatar>
        <v-card-text>
          <p>都内の大学に通う大学３年生です。ソフトテニスが趣味です。</p>
          <p>日々Webアプリの開発に勤しんでいます。</p>
          <p>就活不安や〜</p>
        </v-card-text>

        <v-col class="text-center" cols="12">
          <v-btn
            class="mx-6"
            v-for="icon in icons"
            :key="icon.type"
            :href="icon.url"
            :to="icon.link"
            fab
            dark
            :color="icon.color"
          >
            <v-icon>{{ icon.type }}</v-icon>
          </v-btn>
        </v-col>
      </v-card>
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
      icons: [
        {
          type: "mdi-twitter",
          color: "primary",
          url: "https://twitter.com/youyoutennis928"
        },
        { type: "mdi-github", url: "https://github.com/sftn0928" },
        { type: "mdi-email", color: "secondary", link: "/Contact" }
      ]
    };
  }
};
</script>

<style>
.about-content {
  text-align: center;
}

.about-content {
  padding: 20px 0;
}

/* スマートフォン用 */
@media screen and (max-width: 767px) {
}
</style>
