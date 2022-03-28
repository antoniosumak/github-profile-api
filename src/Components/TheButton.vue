<template>
  <button
    class="bg-lightBlue py-2.5 px-3.5 text-white rounded-md"
    @click="$emit('buttonSubmit')"
  >
    {{ text }}
  </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  components: {},
  props: {
    text: String,
  },
  emits: ['buttonSubmit'],
});
</script>
