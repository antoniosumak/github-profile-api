<template>
  <div class="w-full h-20 lg:h-fit flex items-center space-x-4 lg:space-x-0">
    <img class="h-full rounded-full lg:hidden" :src="avatar_url" />
    <div class="h-full flex flex-col justify-between lg:justify-start w-full">
      <div class="flex items-center justify-between w-full">
        <h2 class="font-bold text-white">{{ name }}</h2>
        <p class="text-white hidden lg:block">
          Joined {{ formatDate(created_at) }}
        </p>
      </div>
      <p class="text-sm text-darkBlue font-bold">@{{ login }}</p>
      <p class="text-white lg:hidden">Joined {{ formatDate(created_at) }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import moment from 'moment';
export default defineComponent({
  components: {},
  props: {
    avatar_url: String,
    name: String,
    login: String,
    created_at: Date,
  },
  methods: {
    formatDate(created: Date | undefined) {
      return moment(created).format('DD MMM YYYY');
    },
  },
});
</script>
