<template>
  <DrawerLayout>
    <template v-slot:header>
      <div class="mx-2 flex-1 px-2">
        <NuxtLink class="font-bold" href="/">Yorgo</NuxtLink>
      </div>
      <div class="flex-none mx-2 px-2">
        <ThemeSelector />
      </div>
    </template>
    <template v-slot:bar>
      <Sidebar />
    </template>
    <template v-slot:body>
      <NuxtPage />
    </template>
  </DrawerLayout>
</template>
