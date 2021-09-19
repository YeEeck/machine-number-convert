<template>
  <div class="home">
    <v-app>
      <v-app-bar
        absolute
        color="indigo darken-2"
        dark
        shrink-on-scroll
        prominent
        scroll-target="#scrolling-techniques"
      >
        <v-app-bar-nav-icon></v-app-bar-nav-icon>

        <v-app-bar-title style="width: 10rem">机器数转换器</v-app-bar-title>

        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </v-app-bar>
      <div class="scroll-warp" id="scrolling-techniques" ref="warp1">
        <v-container class="scroll-box-inner">
          <y-main></y-main>
        </v-container>
      </div>
    </v-app>
  </div>
</template>

<script>
import Main from "@/components/main";
export default {
  name: "Home",
  components: {
    "y-main": Main,
  },
  mounted() {
    this.$refs.warp1.style.height = window.innerHeight - 1 + "px";
  },
};
</script>

<style>
.home {
}
.scroll-warp {
  overflow-y: auto !important;
  padding-top: 129px;
}
</style>
