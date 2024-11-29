<script setup lang="ts">
import Close from "@/components/Close.vue";
</script>

<template>
  <div class="inputs-container">
    <div class="inputs">
      <div>
        <label for="">
          عنوان
          <span class="star">*</span>
        </label>
        <input type="text" placeholder="مثال: نام محصول" />
      </div>

      <div>
        <label for="">
          توضیحات
          <span class="star">*</span>
        </label>
        <input type="text" placeholder="مثال: رنگ محصول، قیمت" />
      </div>
    </div>

    <div class="buttons d-flex justify-space-between align-center my-4">
      <span> دکمه ها </span>

      <div class="line border-sm" />

      <div class="add-button d-flex align-center">
        <svg
          width="20"
          height="20"
          viewBox="0 0 16 16"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M12 8.5H4C3.72667 8.5 3.5 8.27333 3.5 8C3.5 7.72667 3.72667 7.5 4 7.5H12C12.2733 7.5 12.5 7.72667 12.5 8C12.5 8.27333 12.2733 8.5 12 8.5Z"
            fill="#BE0183"
          />
          <path
            d="M8 12.5C7.72667 12.5 7.5 12.2733 7.5 12V4C7.5 3.72667 7.72667 3.5 8 3.5C8.27333 3.5 8.5 3.72667 8.5 4V12C8.5 12.2733 8.27333 12.5 8 12.5Z"
            fill="#BE0183"
          />
        </svg>
        <span class="text"> افزودن </span>
      </div>
    </div>

    <div class="table">
      <div class="thead">
        <div>
          <span>نام دکمه</span>
          <span class="star">*</span>
          <span class="question">؟</span>
        </div>
        <div>
          <span>لینک</span>
          <span class="question">؟</span>
        </div>
        <div>
          <span>عملیات</span>
        </div>
      </div>
      <div class="tbody">
        <div v-for="_ in 3" :key="_">
          <span>نام دکمه را وارد کنید</span>
          <span>لینک دکمه را وارد کنید</span>
          <span><Close /></span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.thead {
  display: flex;
  justify-content: space-between;
  background-color: #f9f9f9;
  border-radius: 4px;
  padding: 8px;
}

.thead div,
.tbody div {
  display: flex;
  align-items: center;
}

.tbody div {
  flex-grow: 1;
  justify-content: space-between;
  padding: 4px 8px;
  border-bottom: 1px solid #ddd;
}

.thead div span:first-of-type {
  font-size: 0.5rem;
}
.tbody div span:not(:last-of-type) {
  font-size: 0.5rem;
}

.thead div .question {
  width: 14px;
  height: 14px;
  margin-right: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 0.5rem;
  color: #be0183;
  background-color: #fff5c6;
  border-radius: 50%;
}

label,
.star {
  font-size: 0.7rem;
}

label {
  margin-bottom: 4px;
}

.star {
  color: #c30000;
}

.inputs-container {
  padding: 8px;
}

.inputs > div {
  display: flex;
  flex-direction: column;
  margin-bottom: 8px;
}

.inputs > div input {
  background-color: #f3f3f3;
  padding: 8px;
  border-radius: 4px;
}
.inputs > div input::placeholder {
  font-size: 10px;
  color: #d7d7d7;
}

.buttons > span:first-of-type {
  color: #353535;
  font-weight: 700;
  font-size: 0.75rem;
}

.line {
  width: 55%;
  height: 1px;
  border-color: #ededed;
}

.add-button .text {
  color: #be0183;
  margin-right: 4px;
}
</style>
