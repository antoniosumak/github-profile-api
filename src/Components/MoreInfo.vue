<template>
  <div class="mt-4 grid grid-cols-1 md:grid-cols-2 gap-4">
    <div class="flex space-x-4 items-center">
      <div class="w-4 h-4 flex items-center justify-center">
        <i class="fa-solid fa-location-dot text-xl text-white"></i>
      </div>
      <p class="text-darkGray text-sm">
        {{ location ? location : 'Not Available' }}
      </p>
    </div>
    <div class="flex space-x-4 items-center">
      <div class="w-4 h-4 flex items-center justify-center">
        <i class="fa-brands fa-twitter text-xl text-white"></i>
      </div>
      <p class="text-darkGray text-sm">
        {{ twitter_username ? twitter_username : 'Not Available' }}
      </p>
    </div>
    <div class="flex space-x-4 items-center">
      <div class="w-4 h-4 flex items-center justify-center">
        <i class="fa-solid fa-link text-xl text-white"></i>
      </div>
      <p class="text-darkGray text-sm">{{ blog ? blog : 'Not Available' }}</p>
    </div>
    <div class="flex space-x-4 items-center">
      <div class="w-4 h-4 flex items-center justify-center">
        <i class="fa-solid fa-building text-xl text-white"></i>
      </div>
      <p class="text-darkGray text-sm">
        @{{ company ? company : 'Not Available' }}
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  components: {},
  props: {
    company: String,
    twitter_username: String,
    location: String,
    blog: String,
  },
});
</script>
