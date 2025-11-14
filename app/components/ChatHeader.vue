<template>
  <UDashboardNavbar title="Hub Chat">
    <template #trailing>
      <UTooltip
        v-if="!clearDisabled"
        text="Clear chat"
      >
        <UButton
          color="neutral"
          variant="subtle"
          icon="i-lucide-trash-2"
          @click="$emit('clear')"
        />
      </UTooltip>
    </template>
    <template #right>
      <UColorModeSelect />
      <UButton
        icon="i-simple-icons-github"
        color="neutral"
        variant="ghost"
        to="https://github.com/ra-jeev/hub-chat"
        target="_blank"
      />
    </template>
  </UDashboardNavbar>
</template>

<script setup lang="ts">
defineEmits(['clear']);

defineProps({
  clearDisabled: {
    type: Boolean,
    default: true,
  },
});
</script>
