<script lang="ts" setup>
import MessageSearch from "@/components/icons/MessageSearch.vue";
import MessageEqual from "@/components/MessageEqual.vue";
import CustomRadio from "@/components/custom/Radio.vue";

const props = defineProps<{
  label: string;
  icon: string;
}>();

const getComponent = (icon: string) => {
  if (icon === "MessageSearch") return MessageSearch;
  else if (icon === "MessageEqual") return MessageEqual;
};
</script>

<template>
  <div></div>
  <!-- <VRadio value="Google" color="primary">
    <template #label>
      <div class="d-flex align-center">
        <component :is="getComponent(props.icon)" />
        <span class="mr-1">{{ props.label }}</span>
      </div>
    </template>
  </VRadio> -->
</template>

