<template>
  <button class="btn bg-primary/35">
    <ContentSlot :use="$slots.default" />
  </button>
</template>
