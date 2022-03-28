<template>
  <div
    class="w-full rounded-md overflow-hidden mb-6 relative bg-lighter flex p-2 items-center justify-between"
  >
    <search-icon class="h-12 w-12 text-lightBlue" />
    <input
      class="w-full py-4 indent-2 h-full bg-lighter"
      placeholder="Search GitHub username ..."
      @input="$emit('update:modelValue', ($event.target as HTMLInputElement).value)"
    />
    <the-button text="Search" @button-submit="$emit('buttonSubmit')" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
//@ts-ignore
import { SearchIcon } from '@heroicons/vue/solid';
import TheButton from './TheButton.vue';
export default defineComponent({
  components: { TheButton, SearchIcon },
  emits: ['update:modelValue', 'buttonSubmit'],
});
</script>
