<script lang="ts" setup>
import CustomSwitch from "@/components/custom/Switch.vue"

const isSwitchOn = ref<boolean>(false)
</script>

<template>
  <div class="bottom d-flex align-center justify-space-between">
    <p class="text-black">
      لایک دستورهای ارسالی کاربران
    </p>
    <CustomSwitch v-model="isSwitchOn" />
  </div>
</template>

<style scoped>
p {
  margin: 0 !important;
  font-size: 0.825rem;
}
</style>
