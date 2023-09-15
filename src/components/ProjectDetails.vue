<template>
  <div>
    <HeaderComp />
    <div class="details">
      <h2 class="details__header">{{ header }}</h2>
      <p class="details__text">{{ text }}</p>
    </div>
    <FooterComp />
  </div>
</template>

<script>
import { mapState } from "vuex";
import HeaderComp from "./HeaderComp.vue";
import FooterComp from "./FooterComp.vue";
export default {
  name: "ProjectDetails",
  data() {
    return {};
  },
  mounted() {},
  methods: {},
  computed: {
    ...mapState(["header", "text"]),
  },
  components: { HeaderComp, FooterComp },
};
</script>

<style lang="scss" scoped></style>
