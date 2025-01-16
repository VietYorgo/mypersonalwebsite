<template>
  <button class="btn btn-primary">
    <ContentSlot :use="$slots.default" />
  </button>
</template>
