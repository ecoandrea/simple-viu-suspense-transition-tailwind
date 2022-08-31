<script setup>
const res = await fetch("https://randomuser.me/api/");
const {results} = await res.json();

const userDB =(results[0]);
console.log(userDB)
</script>

<template>
  <div class="border shadow rounded-md p-4 max-w-sm w-full mx-auto mt-5 flex flex-col item-center">
    <img :src="userDB.picture.large" alt=""  class="rounded-full h-32 w-32"/>
    <h5 class="mt-3">{{userDB.name.first}} - {{userDB.name.last}}</h5>
  
</div>
</template>
