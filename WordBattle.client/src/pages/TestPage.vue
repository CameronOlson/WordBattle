<template>
  <div class="test">
    <fat-banner 
      :id="banner.id"
      :title="banner.title"
      :picture="banner.picture"
      :notification="banner.notification"
      :page="thisPage"
    />
    <div>
      <button type="button" class="btn btn-outline-secondary" @click="updatePage('Home')">Home</button>
      <button type="button" class="btn btn-outline-secondary" @click="updatePage('My Games')">My Games</button>
      <button type="button" class="btn btn-outline-secondary" @click="updatePage('Create Games')">Create Games</button>
      <button type="button" class="btn btn-outline-secondary" @click="updatePage('Search Friends')">Search Friends</button>
    </div>
    <div v-for="button in buttons" :key="button.id">
  <everything-button
      :id="button.id"
      :title="button.title"
      :picture="button.picture"
      :notification="button.notification"
      :page="thisPage"
    ></everything-button>
    </div>
    </div>
</template>

<script>
import EverythingButton from '../components/EverythingButton.vue';
import FatBanner from '../components/FatBanner.vue';

export default {
  components: {
    EverythingButton,
    FatBanner,
  },
  data() {
    return {
      buttons: [
        {
          id: 1,
          title: 'Button 1',
          picture: 'path/to/button1-picture.png',
          notification: true
        },
        {
          id: 2,
          title: 'Button 2',
          picture: 'path/to/button2-picture.png',
          notification: false
        },
        ],
      banner: {
        id: 1,
        title: 'Banner Title',
        picture: 'path/to/banner-picture.png',
        notification: true,
      },
      thisPage: 'Home'
    };
  },
  methods: {
    updatePage(page) {
      console.log("page: ", page)
    }
  }
};
</script>