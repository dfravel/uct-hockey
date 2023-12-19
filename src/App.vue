<script setup>
import PlayerCard from "./components/PlayerCard.vue";
import players from "./data/roster.json";
</script>

<template>
  <div class="grid grid-cols-2 gap-10 px-10">
    <PlayerCard v-for="player in players" :key="player.id" :player="player" />
  </div>
</template>

<style scoped></style>
