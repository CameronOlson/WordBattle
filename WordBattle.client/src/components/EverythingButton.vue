<template>
  <div class="d-grid gap-3 btn-large everythingButton">
    <button class="btn btn-primary" type="button">{{ title }}</button>
    <button class="btn btn-primary" type="button">{{ notification }}</button>
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
 .everythingButton {
  margin: 20px 20px;
  min-height: 20vh;
  border-radius: 50%;
 }

 .Home {  
  margin: 20px 20px;
  min-height: 20vh;
  border-radius: 50%;
 }



/*.homePage {
  border: none;
}

.gamePage {}

.findPage {} */
</style>
