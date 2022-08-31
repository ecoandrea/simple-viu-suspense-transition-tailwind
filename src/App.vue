<script setup>
import UserCard from "./components/UserCard.vue";
import UserCardSkeletor from "./components/UserCardSkeletor.vue";
</script>

<template>
  <h1 class="text-center text-xl">Suspense</h1>
  <Transition
    mode="out-in"
    name="custom-classes"
    enter-active-class="duration-300 ease-out"
    enter-from-class="transform opacity-0"
    enter-to-class="opacity-100"
    leave-active-class="duration-200 ease-in"
    leave-from-class="opacity-100"
    leave-to-class="transform opacity-0"
  >
    <Suspense>
      <UserCard></UserCard>
      <template #fallback>
        <UserCardSkeletor />
      </template>
    </Suspense>
  </Transition>
</template>

<style>
/* we will explain what these classes do next! */

/*
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

*/
</style>
