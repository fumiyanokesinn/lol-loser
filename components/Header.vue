<script setup lang="ts">
  const items = [
    [
      {
        label: 'Home',
        icon: 'i-heroicons-arrow-right-circle-20-solid',
        click: () => navigateTo('/')
      },
      {
        label: 'Profile',
        icon: 'i-heroicons-arrow-right-circle-20-solid',
        click: () => navigateTo('/profile')
      }
    ]
  ];
</script>

<template>
  <header class="sticky top-0 bg-gray-800 lg:px-6 py-2.5 dark:bg-gray-800">
    <div class="flex justify-between items-center lg:mx-14">
      <img
        class="min-w-[14rem]"
        src="/images/Logo/Logo.png"
        alt="Game Planer"
      />
      <ul
        class="hidden lg:flex flex-nowrap flex-col lg:flex-row lg:space-x-8 text-white"
      >
        <li>
          <ULink to="/">Home</ULink>
        </li>
        <li>
          <ULink to="/profile">Profile</ULink>
        </li>
      </ul>
      <ColorMode class="invisible lg:visible" />
      <div class="flex items-center lg:hidden">
        <ColorMode />
        <UDropdown :items="items" :popper="{ placement: 'bottom-start' }">
          <Icon name="prime:align-justify" size="2em" />
        </UDropdown>
      </div>
    </div>
  </header>
</template>
