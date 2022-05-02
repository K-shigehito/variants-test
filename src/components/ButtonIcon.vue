<script setup lang="ts">
import { computed } from 'vue';
import BaseIcon from './icons/BaseIcon.vue';
import IconSearch from './icons/IconSearch.vue';
import IconEdit from './icons/IconEdit.vue';
import IconFavorite from './icons/IconFavorite.vue';

interface Props {
  icon: string;
  width: number | string;
  height: number | string;
}
const props = withDefaults(defineProps<Props>(), {
  icon: '',
  width: 10,
  height: 10,
});

const icons = {
  IconSearch,
  IconEdit,
  IconFavorite,
};
const currentIcon = computed(() => {
  return `Icon${props.icon.charAt(0).toUpperCase() + props.icon.slice(1)}`;
});
</script>

<template>
  <BaseIcon :width="props.width" :height="props.height">
    <component :is="icons[currentIcon]"></component>
  </BaseIcon>
</template>
