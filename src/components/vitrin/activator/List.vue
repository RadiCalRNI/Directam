<script lang="ts" setup>
import ActivatorTag from "./Tag.vue"
</script>

<template>
  <div class="activators-list position-relative px-1 py-4 mt-5 border-sm">
    <span class="px-1 position-absolute">لیست فعال کننده ها</span>
    <div class="d-flex pa-2 flex-wrap">
      <div
        v-for="_ in 3"
        :key="_"
        class="ma-1"
      >
        <ActivatorTag label="عنوان" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.activators-list {
  border-color: #777 !important;
  border-radius: 0.25rem;
}

.activators-list > span:first-of-type {
  top: -0.825rem;
  right: 0.625em;
  background-color: #f8f7fa;
  font-size: 0.75rem;
  color: #757575 !important;
}
</style>
