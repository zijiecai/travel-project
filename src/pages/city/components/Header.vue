<template>
  <div class="header">
    <nav-bar>
      <!-- <router-link tag="div" to="/"> -->
      <div slot="left" class="left" @click="goBack">
        <span class="iconfont back-icon">&#xe6c3;</span>
      </div>
      <!-- </router-link> -->
      <div slot="center" class="center">
        <span class="center-text">城市选择</span>
      </div>
    </nav-bar>
  </div>
</template>
<script>
import NavBar from "components/common/NavBar";

export default {
  name: "CityHeader",
  data() {
    return {};
  },
  methods: {
    goBack() {
      this.$router.push("/");
    },
  },
  components: {
    NavBar,
  },
};
</script>
<style lang="stylus" scoped>
@import '~assets/styles/varibles.styl'

.left
  color #fff
  .back-icon
    font-size 0.4rem
.center
  padding-left 0.38rem
  color #fff
  font-size 0.32rem
  .center-text
    padding 0.12rem 0.6rem
    background-color #fff
    border-radius 0.08rem
    color $bgColor
    font-weight 550
</style>