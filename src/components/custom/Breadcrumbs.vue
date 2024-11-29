<script lang="ts" setup>
import ArrowLeftIcon from "../icons/ArrowLeftIcon.vue";
import { IBreadcrumb } from "@/types/breadcrumb";

const props = defineProps<{
  items: IBreadcrumb[];
}>();
</script>

<template>
  <div class="breadcrumbs-container">
    <ul class="breadcrumbs-ul">
      <li
        v-for="(item, index) in props.items"
        :key="index"
        class="breadcrumbs-items"
      >
        <a
          :href="item.link"
          class="breadcrumb-link"
          :style="{
            color: index === props.items.length - 1 ? '#BE0183' : '#ADADAD',
          }"
        >
          {{ item.title }}
        </a>
        <span
          v-if="index !== props.items.length - 1"
          class="breadcrumb-separator"
        >
          <ArrowLeftIcon width="12" height="12" fill="#adadad" />
        </span>
      </li>
    </ul>
  </div>
</template>

<style scoped>
ul {
  padding: 0;
  margin: 0;
  list-style-type: none;
}

.breadcrumbs-ul {
  display: flex;
  align-items: center;
  gap: 0px;
}

.breadcrumbs-items {
  display: flex;
  align-items: center;
}

.breadcrumb-link {
  text-decoration: none;
  color: #adadad;
  transition: color 0.2s;
  font-size: 12px;
}

.breadcrumb-link:hover {
  color: #be0183;
}

.breadcrumb-separator {
  margin: 0 4px;
  display: flex;
  align-items: center;
}
</style>
