<script lang="ts" setup>
import CloseCircleIcon from "@/components/CloseCircleIcon.vue";
import MoveIcon from "@/components/icons/MoveIcon.vue";
</script>

<template>
  <div class="helper-button">
    <div class="delete-button">
      <CloseCircleIcon />
    </div>
    <div class="move-button">
      <MoveIcon />
    </div>
  </div>
</template>

<style scoped>
.helper-button {
  width: 60px;
  height: 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: absolute;
  top: -12px;
  right: 0;
}

.helper-button > div {
  border-radius: 4px;
  width: 24px;
  height: 24px;
  background-color: #be0183;
  display: flex;
  justify-content: center;
  align-items: center;
}

.helper-button > div:last-of-type {
  box-shadow: 0px 2px 2px 0px #00000040;
}
</style>
