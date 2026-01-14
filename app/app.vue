<script setup lang="ts">
// Components are automatically imported
</script>

<template>
  <header>
    <Show when="signed-out">
      <SignInButton />
    </Show>
    <Show when="signed-in">
      <UserButton />
    </Show>
  </header>

  <main>
    <NuxtPage />
  </main>
</template>
