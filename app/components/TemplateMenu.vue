<template>
  <UDropdownMenu
    v-slot="{ open }"
    :modal="false"
    :items="[
      {
        label: 'Starter',
        to: '#',
      },
      {
        label: 'Landing',
        to: '#',
        color: 'primary',
        checked: true,
        type: 'checkbox',
      },
      {
        label: 'Docs',
        to: '#',
      },
      {
        label: 'SaaS',
        to: '#',
      },
      {
        label: 'Dashboard',
        to: '#',
      },
      {
        label: 'Chat',
        to: '#',
      },
      {
        label: 'Portfolio',
        to: '#',
      },
      {
        label: 'Changelog',
        to: '#',
      },
      {
        label: 'Editor',
        to: '#',
      },
      {
        label: 'Calendar',
        to: '#',
      },
    ]"
    :content="{ align: 'start' }"
    :ui="{ content: 'min-w-fit' }"
    size="xs"
  >
    <UButton
      label="Landing"
      variant="subtle"
      trailing-icon="i-lucide-chevron-down"
      size="xs"
      class="-mb-[6px] truncate rounded-full font-semibold"
      :class="[open && 'bg-primary/15']"
      :ui="{
        trailingIcon: [
          'transition-transform duration-200',
          open ? 'rotate-180' : undefined,
        ]
          .filter(Boolean)
          .join(' '),
      }"
    />
  </UDropdownMenu>
</template>
