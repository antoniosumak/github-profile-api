<template>
  <div
    class="w-full min-h-[300px] bg-lighter rounded-md p-6 lg:flex lg:space-x-4"
  >
    <img
      class="h-20 rounded-full hidden lg:block"
      :src="userData?.avatar_url"
    />
    <div class="w-full">
      <card-header
        :avatar_url="userData?.avatar_url"
        :name="userData?.name"
        :login="userData?.login"
        :created_at="userData?.created_at"
      />
      <p class="my-4 text-white">
        {{ userData?.bio ? userData?.bio : 'This profile has no bio!' }}
      </p>
      <profile-information-grid
        :public_repos="userData?.public_repos"
        :followers="userData?.followers"
        :following="userData?.following"
      />
      <more-info
        :twitter_username="userData?.twitter_username"
        :location="userData?.location"
        :company="userData?.company"
        :blog="userData?.blog"
      />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue';
import CardHeader from './CardHeader.vue';
import ProfileInformationGrid from './ProfileInformationGrid.vue';
import MoreInfo from './MoreInfo.vue';
import { GithubProfile } from '../Services/Types';
export default defineComponent({
  components: { CardHeader, ProfileInformationGrid, MoreInfo },
  props: {
    userData: {
      type: Object as PropType<GithubProfile>,
    },
  },
});
</script>
