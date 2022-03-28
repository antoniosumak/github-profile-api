<template>
  <main-section>
    <div class="w-[90%] md:w-[80%] lg:w-[700px]">
      <the-input v-model="username" @button-submit="searchUsername" />
      <card :user-data="userData"></card>
    </div>
  </main-section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import MainSection from '../Components/MainSection.vue';
import Card from '../Components/Card.vue';
import TheInput from '../Components/TheInput.vue';
import axios from 'axios';
import { GithubProfile } from '../Services/Types';
export default defineComponent({
  components: {
    MainSection,
    Card,
    TheInput,
  },

  data() {
    return {
      username: '',
      userData: {} as GithubProfile,
    };
  },

  async created() {
    const response = await axios.get(
      `https://api.github.com/users/antoniosumak`
    );

    this.userData = response.data;
  },

  methods: {
    async searchUsername() {
      const response = await axios.get(
        `https://api.github.com/users/${this.username}`
      );

      this.userData = response.data;
    },
  },
});
</script>
