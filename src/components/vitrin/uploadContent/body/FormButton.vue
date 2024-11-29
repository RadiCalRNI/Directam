<script lang="ts" setup>
import AddCircleIcon from "@/components/icons/AddCircleIcon.vue";
import ArrowRightIcon from "@/components/icons/ArrowRightIcon.vue";
</script>

<template>
  <div class="form-button">
    <div class="previus">
      <ArrowRightIcon />
    </div>
    <div class="add">
      <AddCircleIcon />
    </div>
  </div>
</template>

<style scoped>
.form-button {
  display: flex;
  justify-content: space-between;
  position: absolute;
  width: calc(100% + 40px);
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%); /* Centers the button container */
}
.form-button > div {
  width: 2rem;
  height: 2rem;
  display: flex;
  background-color: #f9f9f9;
  border-radius: 50%;
  justify-content: center;
  align-items: center;
  border: 1px solid var(--neutral-Gray-2, #f3f3f3);
  box-shadow: 0px 3px 10px 0px #00000033;
}
</style>
