<!-- eslint-disable vue/no-restricted-class -->
<script lang="ts" setup>
import CloseCircle from "@/components/icons/CloseCircle.vue";

const props = defineProps({
  label: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="tag-container">
    <span class="ml-2">{{ props.label }}</span>
    <CloseCircle />
  </div>
</template>

<style scoped>
.tag-container {
  display: flex;
  align-items: center;
  border-radius: 1rem;
  background-color: #ffdcf4;
  padding: 0.25rem 0.5rem;
}

.tag-container span {
  color: #be0183;
  font-size: 0.825rem;
}
</style>
