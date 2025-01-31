<template>
  <div class="card bg-base-200 m-6 shadow-xl">
    <div class="card-body">
      <ContentSlot :use="$slots.default" />
      <div class="card-actions justify-end"></div>
    </div>
  </div>
</template>
