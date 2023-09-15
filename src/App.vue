<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script></script>

<style lang="scss">
#app {
  font-family: "Jost", sans-serif;
  font-family: "DM Serif Display", serif;

  .center {
    padding-left: calc(50% - (1200px / 2));
    padding-right: calc(50% - (1200px / 2));
  }

  a {
    text-decoration: none;
  }
}
</style>
