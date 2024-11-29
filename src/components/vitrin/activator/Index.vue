<script lang="ts" setup>
import VitrinHeader from "../Header.vue";
import VitrinActivatorBody from "./Body.vue";
import VitrinActivatorFooter from "./Footer.vue";
</script>

<template>
  <div class="activator border-sm px-4 py-5">
    <VitrinHeader title="فعال کننده" />
    <VitrinActivatorBody />
    <VitrinActivatorFooter />
  </div>
</template>


<style scoped>
.activator {
  border-radius: 0.75rem;
  border-color: #ededed;
}
</style>
