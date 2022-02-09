<script setup lang="ts">
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
</script>

<template>
  <BaseIcon :width="props.width" :height="props.height">
    <IconSearch v-if="props.icon === 'search'" />
    <IconEdit v-else-if="props.icon === 'edit'" />
    <IconFavorite v-else-if="props.icon === 'favorite'"></IconFavorite>
  </BaseIcon>
</template>
