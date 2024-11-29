
<script lang="ts" setup>
import VitrinActivatorList from "./List.vue"
import CustomRadio from "@/components/custom/Radio.vue"
import MessageSearch from "@/components/icons/MessageSearch.vue"
import MessageEqual from "@/components/MessageEqual.vue"

const model = ref<string>("first")
</script>

<template>
  <div class="body my-4">
    <div class="selection-section">
      <p class="mb-1 font-weight-regular text-black">
        اگر فعال کننده،
      </p>
      <div class="options d-flex justify-space-between">
        <CustomRadio
          id="first"
          v-model="model"
          value="first"
          label="اولین"
          name="equal"
        >
          <template #icon>
            <MessageSearch />
          </template>
        </CustomRadio>
        <CustomRadio
          id="include"
          v-model="model"
          value="include"
          label="شامل"
          name="equal"
        >
          <template #icon>
            <MessageEqual />
          </template>
        </CustomRadio>
      </div>
      <div class="input-container mt-1 py-1 border-sm px-3">
        <label class="activator-text text-black">فعال کننده</label>
        <input
          type="text"
          placeholder="مثال: 10، قیمت"
        >
      </div>
      <VitrinActivatorList />
    </div>
  </div>
</template>

<style scoped>
.input-container {
  border-color: #aaa !important;
  border-radius: 0.25rem;
  display: flex;
  flex-direction: column;
}

.input-container input {
  border: none;
  outline: none;
  font-size: 0.825rem;
}

.input-container input::placeholder {
  font-size: 0.625rem;
  color: #aaa;
}

.activator-text {
  font-size: 0.625rem;
}
.selection-section p {
  font-size: 0.75rem;
  color: #353535;
}
</style>
