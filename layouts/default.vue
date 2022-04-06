<template>
  <v-app dark>
    <div class="header-wrapper my50" v-show="isShow">
      <v-navigation-drawer
        v-model="drawer"
        :clipped="clipped"
        :temporary="temporary"
        fixed
        app
      >
        <v-list>
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            :to="item.to"
            router
            exact
          >
            <v-list-item-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title v-text="item.title" />
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
      <v-app-bar :clipped-left="clipped" class="header" fixed app>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
        <v-spacer />
        <v-toolbar-title v-text="title" class="header-title" />
        <v-spacer />
      </v-app-bar>
    </div>

    <v-container>
        <nuxt />
    </v-container>
    <v-footer class="footer-wrapper" v-if="isShow">
      <v-row justify="center">
        <v-btn
          v-for="(item, i) in items"
          :key="i"
          color="white"
          text
          :to="item.to"
          rounded
          class="mx-2 my-2"
        >
          {{ item.title }}
        </v-btn>
      </v-row>
      <v-col class="text-center" cols="12">
        <v-btn
          class="mx-10"
          v-for="icon in icons"
          :key="icon.type"
          :href="icon.url"
          :to="icon.link"
          fab
          large
          icon
        >
          <v-icon>{{ icon.type }}</v-icon>
        </v-btn>
      </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  // render: {
  //   hideEvent() {
  //     var currentPath = location.pathname;
  //     return currentPath === "/" ? (this.isShow = false) : (this.isShow = true);
  //     console.log(currentPath);
  //   }
  // },
  data() {
    return {
      title: "Welcome to Yosuke's portfolio",
      clipped: false,
      drawer: false,
      temporary: true,
      fixed: false,
      isShow: true,
      items: [
        {
          title: "Top",
          to: "/"
        },
        {
          title: "About",
          to: "/About"
        },
        {
          title: "Career",
          to: "/Career"
        },
        {
          title: "Skill",
          to: "/Skill"
        },
        {
          title: "Works",
          to: "/Works"
        },
        {
          title: "Contact",
          to: "/Contact"
        }
      ],
      icons: [
        { type: "mdi-twitter", url: "https://twitter.com" },
        { type: "mdi-github", url: "https://github.com/sftn0928" },
        { type: "mdi-email", link: "/Contact" }
      ]
    };
  }
};
</script>
<style>
.header-wrapper {
  margin-bottom: 50px;
}

.header-title {
  font-size: 26px;
}

.footer-wrapper {
  margin-top: 50px;
}
</style>
