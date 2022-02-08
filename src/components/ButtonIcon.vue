<script setup lang="ts">
import BaseIcon from './icons/BaseIcon.vue';
import IconSearch from './icons/IconSearch.vue';

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
  <BaseIcon
    :width="props.width"
    :height="props.height"
  >
    <IconSearch />
  </BaseIcon>
</template>
