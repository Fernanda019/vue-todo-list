<script setup lang="ts">
defineProps<{
  isChecked?: boolean
}>()
</script>

<template>
  <label>
    <input
      type="checkbox"
      :checked="isChecked"
    >
    <span>
      <slot />
    </span>
  </label>
</template>

<style scoped>
label {
  cursor: pointer;
}

input:checked + span {
  text-decoration: line-through;
}
</style>