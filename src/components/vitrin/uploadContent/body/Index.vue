<script lang="ts" setup>
import VitrinUploadContentBodyUploadImage from "./UploadImage.vue"
import VitrinUploadContentBodyInputs from "./Inputs.vue"
import VitrinUploadContentBodyHelperButton from "./HelperButton.vue"
import VitrinUploadContentBodyFormButton from "./FormButton.vue"
</script>

<template>
  <div class="form">
    <VitrinUploadContentBodyUploadImage />
    <VitrinUploadContentBodyInputs />
    <VitrinUploadContentBodyHelperButton />
    <VitrinUploadContentBodyFormButton />
  </div>
</template>

<style scoped>
.form {
  position: relative;
  border: 2px solid #ededed;
  border-radius: 0.5rem;
  padding-bottom: 0.825rem;
}
</style>
