<script setup lang="ts">
import BaseIcon from './icons/BaseIcon.vue';
import IconUpdate from './icons/IconUpdate.vue';
import IconCalendar from './icons/IconCalendar.vue';

interface Props {
  icon: string;
}
const props = withDefaults(defineProps<Props>(), {
  icon: '',
});
</script>

<template>
  <BaseIcon
    v-if="props.icon === 'update'"
    icon-name="update"
    :width="10"
    :height="10"
    ><IconUpdate
  /></BaseIcon>
  <BaseIcon
    v-else-if="props.icon === 'calendar'"
    icon-name="calendar"
    :width="10"
    :height="10"
    ><IconCalendar
  /></BaseIcon>
</template>

<style></style>
