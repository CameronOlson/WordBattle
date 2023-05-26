<template>
  <div class="fatBanner">
    <h2>Testing Fat Banner for my Test Page</h2>
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    title: String,
    page: String,
    picture: String,
    notification: String
  },
  setup(props) {
    return {};
  },
};
</script>

<style scoped>
 .fatBanner {
  min-height: 20vh;
 }

/*.homePage {
  border: none;
}

.gamePage {}

.findPage {} */
</style>
