<script setup lang="ts">
interface Player {
  name: string;
  number: number;
  position: string;
  hometown: string;
  shop: string;
  grade: string;
  image: string;
}

const props = defineProps({
  player: {
    type: Object as PropType<Player>,
    required: true
  }
});
</script>

<template>
  <div class="flex bg-white shadow-lg rounded-lg overflow-hidden">
    <div class="w-1/3">
      <img :src="props.player.image" alt="" class="object-cover w-full h-full" />
    </div>
    <div class="w-2/3 p-4 relative">
      <span class="absolute top-4 right-4 bg-blue-500 text-white rounded-full px-3 py-1.5 text-base"> {{ player.number }} </span>
      <h2 class="text-xl font-semibold">{{ player.name }}</h2>
      <p class="text-gray-600">{{ player.position }}</p>
      <p class="text-gray-600">{{ player.hometown }}</p>
      <p class="text-gray-600">{{ player.shop }}</p>
      <p class="text-gray-600">{{ player.grade }}</p>
    </div>
  </div>
</template>

<style scoped></style>
