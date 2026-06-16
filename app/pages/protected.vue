<script setup lang="ts">
// `/api/auth` reads the session on the server via `event.context.auth()` and
// returns a 401 if the user is not signed in. Unlike the `<SignedIn>` component,
// which only controls what renders, this is the real access check.
const { data, error } = await useFetch<{ userId: string }>('/api/auth')

if (error.value) {
  await navigateTo('/')
}
</script>

<template>
  <p>Welcome! Your user ID is <code>{{ data?.userId }}</code>.</p>
</template>
