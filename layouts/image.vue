<script setup lang="ts">
import { defineComponent, computed } from 'vue'
import Default from '../layouts/default.vue'
import { handleBackground } from '../layoutHelper'
const props = defineProps({
  image: {
    type: String,
  },
})
const style = computed(() => handleBackground(props.image))
const components = defineComponent({ Default })
</script>

<template>
  <div class="slidev-layout w-full h-full" :style="style">
    <slot />
  </div>
</template>