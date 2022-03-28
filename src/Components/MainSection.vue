<template>
  <section
    class="w-full min-h-screen bg-dark flex items-center justify-center flex-col"
  >
    <slot></slot>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  components: {},
});
</script>
