<!-- TODO: universe a no-underline -->
<template>
  <NuxtLink :href="props.href" :target="props.target" class="no-underline">
    <span class="text-sm lg:text-md">🔗</span> <slot />
  </NuxtLink>
</template>

<script setup lang="ts">
import type { PropType } from "vue";

const props = defineProps({
  href: {
    type: String,
    default: "",
  },
  target: {
    type: String as PropType<
      | "_blank"
      | "_parent"
      | "_self"
      | "_top"
      | (string & object)
      | null
      | undefined
    >,
    default: undefined,
    required: false,
  },
});
</script>
