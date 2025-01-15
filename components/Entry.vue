<script setup>
defineProps(["list"]);
</script>

<template>
  <li v-for="article in list" :key="article._path">
    <details v-if="article.children">
      <summary>
        <NuxtLink v-if="article._path" :href="article._path">
          {{ article.title }}
        </NuxtLink>
        <!-- TODO: name -->
        <span v-else>
          {{ article.title }}
        </span>
      </summary>
      <ul>
        <Entry :list="article.children" />
      </ul>
    </details>
    <!-- TODO: do not refresh -->
    <NuxtLink v-else :href="article._path">
      {{ article.title }}
    </NuxtLink>
  </li>
</template>
