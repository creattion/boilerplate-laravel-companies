<script lang="ts" setup>
withDefaults(
  defineProps<{
    text?: string;
    size?: number;
  }>(),
  {
    text: 'Carregando...',
    size: 20,
  },
);
</script>

<template>
  <div class="flex flex-row items-center gap-2">
    <svg
      :height="size"
      :width="size"
      class="fill-primary"
      viewBox="0 0 24 24"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        class="spinner-loading"
        d="M12,4a8,8,0,0,1,7.89,6.7A1.53,1.53,0,0,0,21.38,12h0a1.5,1.5,0,0,0,1.48-1.75,11,11,0,0,0-21.72,0A1.5,1.5,0,0,0,2.62,12h0a1.53,1.53,0,0,0,1.49-1.3A8,8,0,0,1,12,4Z"
      />
    </svg>

    {{ text }}
  </div>
</template>

<style scoped></style>
