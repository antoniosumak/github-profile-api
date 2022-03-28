<template>
  <div
    class="grid grid-cols-3 bg-dark text-white p-4 gap-2 place-items-center rounded-md"
  >
    <div class="flex items-center flex-col justify-center">
      <p class="text-[11px]">Repos</p>
      <h2>{{ public_repos }}</h2>
    </div>
    <div class="flex items-center flex-col justify-center">
      <p class="text-[11px]">Followers</p>
      <h2>{{ followers }}</h2>
    </div>
    <div class="flex items-center flex-col justify-center">
      <p class="text-[11px]">Following</p>
      <h2>{{ following }}</h2>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  components: {},
  props: {
    public_repos: Number,
    following: Number,
    followers: Number,
  },
});
</script>
