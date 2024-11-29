<script lang="ts" setup>
import CardAddIcon from '@/components/CardAddIcon.vue'
</script>

<template>
  <div class="add-item">
    <VBtn color="primary">
      <span class="text">افزودن آیتم ویترین عمودی</span>
      <CardAddIcon />
    </VBtn>
  </div>
</template>

<style scoped>
.add-item {
  margin-top: 8px;
}
.add-item .text {
  font-size: 0.825rem;
  margin-left: 0.5rem
}

.add-item button {
  width: 100%;
}
</style>
