<script setup lang="ts">
import Default from '../layouts/default.vue'
import { defineComponent } from 'vue'
import { computed } from 'vue'
import { handleBackground } from '../layoutHelper'
import Fact from "./fact.vue";

const props = defineProps({
  background: {
    // random image from a curated Unsplash collection by Anthony
    default: 'https://source.unsplash.com/collection/94734566/1920x1080',
  },
})

const style = computed(() => handleBackground(props.background, true))
const components = defineComponent({ Default })
</script>

<template>
  <default class="cover text-center" :style="style">
    <slot />
  </default>
</template>

