<script setup lang="ts">
const links = [
  { label: "Docs", to: "#", target: "_blank" },
  { label: "GitHub", to: "#", target: "_blank" },
  { label: "Twitter", to: "#", target: "_blank" },
  { label: "Status", to: "#" },
  { label: "Privacy", to: "#" },
];
</script>

<template>
  <UFooter
    :ui="{
      container: 'border-t border-default lg:py-8',
      right: 'gap-x-0 flex-wrap',
    }"
  >
    <template #left>
      <p class="text-sm text-dimmed">
        Built with Nuxt UI • © {{ new Date().getFullYear() }}
        <a
          class="text-sm text-dimmed ml-2"
          href="https://beian.miit.gov.cn/#/Integrated/index"
        >
          冀ICP备19030464号-1
        </a>
      </p>
    </template>

    <template #right>
      <UButton
        v-for="link in links"
        :key="link.label"
        :label="link.label"
        :to="link.to"
        color="neutral"
        variant="link"
        class="font-light"
        size="sm"
      />
    </template>
  </UFooter>
</template>
