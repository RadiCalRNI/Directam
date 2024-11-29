
<script lang="ts" setup>
const props = defineProps({
  modelValue: {
    type: Boolean,
    required: true,
  },
  color: {
    type: String,
    default: "be1083",
  },
});
const emit = defineEmits(["update:modelValue"]);

const localValue = ref(props.modelValue);

watch(
  () => props.modelValue,
  (newValue) => {
    localValue.value = newValue;
  }
);

watch(localValue, (newValue) => {
  emit("update:modelValue", newValue);
});

const toggle = () => {
  localValue.value = !localValue.value;
};
</script>

<template>
  <div
    class="custom-switch"
    :class="{ checked: localValue }"
    :style="{ backgroundColor: props.color }"
    @click="toggle"
  >
    <span class="switch-handle"></span>
  </div>
</template>


<style scoped>
/* استایل کلی سوییچ */
.custom-switch {
  width: 40px;
  height: 20px;
  border-radius: 25px;
  background-color: #ccc;
  display: flex;
  align-items: center;
  position: relative;
  padding: 3px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

/* وقتی سوییچ فعال است */
.custom-switch.checked {
  background-color: #be1083; /* رنگ سوییچ فعال */
}

/* دسته سوییچ */
.custom-switch .switch-handle {
  width: 14px;
  height: 14px;
  background-color: #fff;
  border-radius: 50%;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
  position: absolute;
  left: 4px;
  transform: translateX(0); /* حالت پیش‌فرض */
  transition: all 0.3s ease; /* اضافه کردن انیمیشن نرم */
}

/* تغییر حالت دسته هنگام فعال شدن */
.custom-switch.checked .switch-handle {
  /* transform: translateX(18px);  */
  /* انتقال دسته به سمت راست */
  left: 22px;
}
</style>

