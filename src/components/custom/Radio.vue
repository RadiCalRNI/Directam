<script lang="ts" setup>
// Define props using the `defineProps` function
const props = defineProps({
  value: {
    type: [String, Number],
    required: true,
  },
  label: {
    type: String,
    required: true,
  },
  modelValue: {
    type: [String, Number],
    default: "",
  },
  disabled: {
    type: Boolean,
    default: false,
  },
  id: {
    type: String,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
});
const emit = defineEmits(["update:modelValue"]);

// Define a computed property to handle two-way binding with modelValue
const localValue = computed({
  get() {
    return props.modelValue; // Return the modelValue prop
  },
  set(value) {
    emit("update:modelValue", value); // Emit the updated value to the parent
  },
});
</script>

<template>
  <div class="custom-radio">
    <input
      :id="id"
      v-model="localValue"
      type="radio"
      :value="value"
      :checked="localValue === value"
      :disabled="disabled"
      :name="name"
    />
    <label :for="id" :class="{ checked: localValue === value }">
      <span class="icon" />
      <span class="content mr-1">
        <slot name="icon" />
        <span class="mr-1">{{ label }}</span>
      </span>
    </label>
  </div>
</template>

<style scoped>

.custom-radio input[type="radio"] {
  display: none;
}

.custom-radio label {
  position: relative;
  display: flex;
  align-items: center;
  cursor: pointer;
  font-size: 16px;
  line-height: 20px;
}

.custom-radio label .icon {
  width: 20px;
  height: 20px;
  border-radius: 50%;
  border: 2px solid #ccc;
  background-color: white;
  position: relative;
  transition: background-color 0.3s ease;
  display: flex;
  justify-content: center;
  align-items: center;
}

.custom-radio input[disabled] + label .icon {
  background-color: #eee;
}

.custom-radio label.checked .icon {
  background-color: #fff;
  border-color: #9c1c77;
  transition: background-color 2.3s ease;
}

.custom-radio label.checked .icon::after {
  content: "";
  width: 100%;
  height: 100%;
  border-radius: 50%;
  transition: background-color 0.3s ease;
  background-color: #9c1c77;
  border: 1px solid #fff;
}

.custom-radio .content {
  display: flex;
  align-items: center;
}
</style>
