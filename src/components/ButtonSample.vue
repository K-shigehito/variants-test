<script setup lang="ts">
import BaseButton from './BaseButton.vue';
const handleClick = () => {
  alert('clicked');
};
</script>

<template>
  <div class="m-4 space-y-4">
    <div class="flex items-center gap-4">
      <BaseButton type="primary" size="small" @click="handleClick">
        Button
      </BaseButton>
      <BaseButton type="primary" size="middle" @click="handleClick">
        Button
      </BaseButton>
      <BaseButton type="primary" size="large" @click="handleClick">
        Button
      </BaseButton>
    </div>

    <div class="flex items-center gap-4">
      <BaseButton
        type="primary"
        size="small"
        icon="search"
        @click="handleClick"
      >
        Button
      </BaseButton>
      <BaseButton
        type="primary"
        size="middle"
        icon="search"
        @click="handleClick"
      >
        Button
      </BaseButton>
      <BaseButton
        type="primary"
        size="large"
        icon="search"
        @click="handleClick"
      >
        Button
      </BaseButton>
    </div>

    <div class="flex items-center gap-4">
      <BaseButton type="outline" size="small" @click="handleClick">
        Button
      </BaseButton>
      <BaseButton type="outline" size="middle" @click="handleClick">
        Button
      </BaseButton>
      <BaseButton type="outline" size="large" @click="handleClick">
        Button
      </BaseButton>
    </div>

    <div class="flex items-center gap-4">
      <BaseButton
        type="outline"
        size="small"
        icon="search"
        @click="handleClick"
      >
        Button
      </BaseButton>
      <BaseButton
        type="outline"
        size="middle"
        icon="search"
        @click="handleClick"
      >
        Button
      </BaseButton>
      <BaseButton
        type="outline"
        size="large"
        icon="search"
        @click="handleClick"
      >
        Button
      </BaseButton>
    </div>
  </div>
</template>

<style></style>
