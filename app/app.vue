<script setup lang="ts"></script>

<template>
    <header>
      <SignedOut>
        <SignInButton mode="modal" />
      </SignedOut>
      <SignedIn>
        <UserButton />
      </SignedIn>
    </header>

    <main>
        <NuxtPage />
    </main>
</template>
