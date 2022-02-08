<script setup lang="ts">
interface Props {
  iconName: string;
  width: number | string;
  height: number | string;
  iconColor: string;
}
const props = withDefaults(defineProps<Props>(), {
  iconName: '',
  width: 20,
  height: 20,
  iconColor: 'currentColor',
});
</script>
<template>
  <svg
    xmlns="http://www.w3.org/2000/svg"
    :width="props.width"
    :height="props.height"
    x="0px"
    y="0px"
    viewBox="0 0 20 20"
    :aria-labelledby="props.iconName"
    role="presentation"
  >
    <title :id="props.iconName" lang="en">{{ props.iconName }} icon</title>
    <g :fill="props.iconColor">
      <slot />
    </g>
  </svg>
</template>

<style scoped>
svg {
  display: inline-block;
  vertical-align: baseline;
  margin-bottom: -2px;
}
</style>
