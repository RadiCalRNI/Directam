<script lang="ts" setup>
import InfoCircle from "@/components/icons/InfoCircleIcon.vue";

const props = defineProps({
  title: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="top">
    <div class="d-flex mb-1 justify-space-between align-center">
      <h3 class="text-primary">
        {{ props.title }}
      </h3>
      <span class="text-grey-darken-1 d-flex align-center">
        <InfoCircle />
        <span class="help mr-2">راهنمایی</span>
      </span>
    </div>
    <div class="progress-bar">
      <VProgressLinear model-value="55" color="primary" height="5" />
    </div>
    <p class="mt-3 subtitle-text text-grey-lighten-1">
      منظور از فعال کننده، همان پیامی است که کاربر برای شما در دایرکت ارسال می
      کند تا ویترین ارسال شود.
    </p>
  </div>
</template>


<style scoped>
.subtitle-text {
  font-size: 0.5rem;
  font-weight: lighter;
  margin-top: 0.25rem !important;
}

.help {
  font-size: 0.75rem;
}
</style>
