<script setup lang="ts">
import GallaryAdd from '@/components/GallaryAdd.vue'

</script>

<template>
  <div class="upload-image">
    <input
      id="myfile"
      type="file"
      name="myfile"
    >
    <div class="upload-image-preview pa-3 text-center bg-blue-grey-lighten-5">
      <GallaryAdd />
      <div class="description">
        <p>برای بارگذاری تصویر کلیک کنید.</p>
        <div class="rules">
          <p>فرمت های مجاز JPEG, JPG, Png</p>
          <p>حداکثر اندازه عکس 8MB</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.upload-image {
  height: 118px;
  position: relative;
}

.upload-image input {
  height: 100%;
  width: 100%;
  opacity: 0;
  position: absolute;
}

.upload-image .upload-image-preview {
  height: 100%;
  width: 100%;
}

.description p:first-of-type {
  font-size: 0.625rem;
  margin: 0;
  line-height: 18px;
}
.description .rules {
  margin-top: 1px;
}
.description .rules p:first-of-type {
  font-size: 0.5rem;
  margin: 0;
  color: #757575

}
.description .rules p:last-of-type {
  font-size: 0.625rem;
  margin: 0;
  color: #757575

}
</style>
