<script setup lang="ts">
import BaseButton from './BaseButton.vue';
const handleClick = () => {
  alert('clicked');
};
</script>

<template>
  <div class="m-4 space-y-4">
    <div class="space-x-4">
      <BaseButton
        type="primary"
        size="small"
        icon="update"
        @click="handleClick"
      >
        Button
      </BaseButton>
      <BaseButton
        type="primary"
        size="middle"
        icon="calendar"
        @click="handleClick"
      >
        Button
      </BaseButton>
      <BaseButton type="primary" size="large" @click="handleClick">
        Button
      </BaseButton>
    </div>
    <div class="space-x-4">
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
  </div>
</template>

<style></style>
