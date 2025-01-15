<template>
  <div class="gallery">
    <ContentSlot :use="$slots.default" unwrap="p" />
  </div>
</template>

<!-- copied from original files -->
<style scoped>
.gallery {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
  padding: 10px;
  max-width: 600px;
  margin: 0 auto;
}

.gallery img {
  width: 100%;
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.3);
}
</style>
