<template>
  <v-container>
    <v-row :align="alignment" :justify="justify">
      <v-col cols="6" md="3" v-for="(item, index) in items" :key="index">
        <div class="fade-in-el" v-scroll-inview:fadeIn>
          <div class="skill-content">
            <v-img
              class="skill-icon"
              max-height="200px"
              :src="item.svg"
              alt="アイコン画像"
            ></v-img>
            <p>{{ item.name }}</p>
            <p class="star">{{ item.level }}</p>
            <p>{{ item.career }}</p>
          </div>
        </div>
      </v-col>
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
      }
    };
  }
};
</script>

<style>
.skill-content {
  text-align: center;
  max-width: 200px;
  margin: 0 auto;
}

.skill-icon {
  margin-bottom: 20px;
}

.star {
  color: yellow;
}
</style>
