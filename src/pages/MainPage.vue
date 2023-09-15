<template>
  <div class="main">
    <HeaderComp />
    <MainComp />
    <FooterComp />
  </div>
</template>

<script>
import FooterComp from "@/components/FooterComp.vue";
import HeaderComp from "@/components/HeaderComp.vue";
import MainComp from "@/components/MainComp.vue";

export default {
  name: "MainPage",
  data() {
    return {};
  },
  mounted() {},
  methods: {},
  components: { FooterComp, HeaderComp, MainComp },
};
</script>

<style lang="scss" scoped></style>
