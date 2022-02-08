<script setup lang="ts">
import { computed } from 'vue';

interface Props {
  type: 'primary' | 'outline';
  size: 'small' | 'middle' | 'large';
  icon: boolean;
}
interface Emits {
  (e: 'click'): void;
}

const props = withDefaults(defineProps<Props>(), {
  type: 'primary',
  size: 'small',
  icon: false,
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
const iconClass = computed(() => (props.icon ? ' after:content-["■"]' : ''));
</script>

<template>
  <button
    class="font-roboto"
    :class="[typeClass, sizeClass, iconClass]"
    @click="handleClick"
  >
    <slot />
  </button>
</template>

<style></style>
