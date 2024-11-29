<script lang="ts"setup>
import VitrinActivator from "@/components/vitrin/activator/Index.vue";
import VitrinUploadContent from "@/components/vitrin/uploadContent/Index.vue";
import TickCircle from "@/components/icons/TickCircle.vue";
import EyeIcon from "@/components/icons/EyeIcon.vue";
import CustomBreadcrumbs from "@/components/custom/Breadcrumbs.vue";
import { IBreadcrumb } from "@/types/breadcrumb";


const items = ref<IBreadcrumb[]>([
  {
    title: "امکانات",
    link: "https://varzesh3.com",
  },
  {
    title: "ویترین ساز",
    link: "https://google.com",
  },
]);
</script>

<template>
  <div class="vitrin-container">
    <CustomBreadcrumbs :items="items" class="mb-4" />
    <VitrinActivator />
    <VitrinUploadContent class="mt-4" />
    <div class="mt-2 d-flex w-100 justify-space-between">
      <VBtn variant="outlined" color="primary" class="d-flex align-center w-25">
        <EyeIcon fill="#BE0183" width="20" height="20" />
      </VBtn>
      <VBtn color="primary" class="d-flex align-center w-66">
        <TickCircle />
        <span class="mr-2"> ذخیره </span>
      </VBtn>
    </div>
  </div>
</template>


<style scoped>
.vitrin-container {
}
</style>
