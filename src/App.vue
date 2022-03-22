<template>
  <div class="p-20">
    <ul>
      <li v-for="user of state.users">{{ user.name }}</li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { reactive } from 'vue';

const state = reactive<{ users: any[] }>({ users: [] });

async function fetchUsers() {
  state.users = await (await fetch('https://restapi.fr/api/vueusers')).json();
}

fetchUsers();
</script>

<style lang="scss"></style>
