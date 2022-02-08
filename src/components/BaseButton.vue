<script setup lang="ts">
import { computed } from 'vue';
import ButtonIcon from './ButtonIcon.vue';

interface Props {
  type: 'primary' | 'outline';
  size: 'small' | 'middle' | 'large';
  icon?: string;
}
interface Emits {
  (e: 'click'): void;
}

const props = withDefaults(defineProps<Props>(), {
  type: 'primary',
  size: 'small',
  icon: '',
});
const emit = defineEmits<Emits>();

const handleClick = () => {
  emit('click');
};

const typeClass = computed(() => {
  if (props.type === 'primary') {
    return 'bg-emerald-600 text-emerald-50 hover:bg-emerald-800';
  } else if (props.type === 'outline') {
    return 'border border-emerald-800 text-emerald-800 hover:bg-emerald-50';
  } else {
    return '';
  }
});
const sizeClass = computed(() => {
  if (props.size === 'small') {
    return 'text-sm px-3.5 py-1.5 rounded';
  } else if (props.size === 'middle') {
    return 'text-md px-5 py-2 rounded-md';
  } else if (props.size === 'large') {
    return 'text-lg px-6 py-2.5 rounded-lg';
  } else {
    return '';
  }
});
const iconSize = computed(() => {
  if (props.size === 'small') {
    return 16;
  } else if (props.size === 'middle') {
    return 21;
  } else if (props.size === 'large') {
    return 28;
  } else {
    return '';
  }
});
</script>

<template>
  <button
    class="flex items-center gap-2.5 font-roboto"
    :class="[typeClass, sizeClass]"
    @click="handleClick"
  >
    <slot />
    <ButtonIcon
      v-if="props.icon"
      :icon="props.icon"
      :width="iconSize"
      :height="iconSize"
    ></ButtonIcon>
  </button>
</template>

<style></style>
