<script setup lang="ts">
import BaseIcon from './icons/BaseIcon.vue';
import IconSearch from './icons/IconSearch.vue';
import IconCalendar from './icons/IconCalendar.vue';

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
    v-if="props.icon === 'search'"
    icon-name="search"
    :width="props.width"
    :height="props.height"
  >
    <IconSearch />
  </BaseIcon>
  <BaseIcon
    v-else-if="props.icon === 'calendar'"
    icon-name="calendar"
    :width="props.width"
    :height="props.height"
  >
    <IconCalendar />
  </BaseIcon>
</template>

<style></style>
