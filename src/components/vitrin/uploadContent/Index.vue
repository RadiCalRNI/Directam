<script lang="ts" setup>
import VitrinHeader from "../Header.vue";
import VitrinUploadContentBody from "./body/Index.vue";
import VitrinUploadContentFooter from "./Footer.vue";
</script>

<template>
  <div class="upload-content border-sm px-3 pb-2 pt-5">
    <VitrinHeader title="بارگذاری محتوا" />
    <VitrinUploadContentBody />
    <VitrinUploadContentFooter />
  </div>
</template>

<style scoped>
.upload-content {
  border-radius: 0.75rem;
  border-color: #ededed;
}
</style>
