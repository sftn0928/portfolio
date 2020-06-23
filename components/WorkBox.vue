<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="6" v-for="(item, index) in items" :key="index">
        <div class="fade-in-el" v-scroll-inview:fadeIn>
        <v-card class="mx-auto work-card" max-width="400" outlined tile>
          <v-img
            class="white--text align-end"
            height="auto"
            :src="item.imgUrl"
            alt="イメージ画像"
          >
          </v-img>
          <v-card-title>{{ item.title }}</v-card-title>
          <v-card-text class="text--primary">
            <div>{{ item.sentence }}</div>
          </v-card-text>
          <v-card-actions>
            <v-btn
              class="work-btn"
              color="secondary"
              :href="item.workUrl"
              target="_blank"
              rel="noopner"
              @click.stop="item.workUrl === '' ? dialog = true : dialog = false"
              >詳細
            </v-btn>
          </v-card-actions>
        </v-card>
        </div>
      </v-col>
      <v-dialog v-model="dialog" max-width="400">
        <v-card work-card>
          <v-card-title>まだリリースしてません!</v-card-title>
          <v-card-text>
            気長に待っててね。
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="secondary" text @click="dialog = false">
              OK!
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: {
    items: Array
  },
  data() {
    return {
      fadeInOption: {
        delay: 5
      },
      item: Object,
      dialog: false
    };
  }
};
</script>

<style>
.work-card {
  margin-bottom: 40px;
}
.work-card:hover {
  box-shadow: 0 0 15px rgba(117, 117, 117, 0.253);
}

.work-btn {
  margin: 10px auto;
  text-align: center;
}
</style>
