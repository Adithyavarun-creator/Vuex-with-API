<template>
  <div class="bg-white shadow rounded-xl">
    <router-link :to="{ name: 'mealDetails', params: { id: meal.idMeal } }">
      <img
        :src="meal.strMealThumb"
        alt="strMeal"
        class="rounded-t-2xl h-48 w-full object-cover"
      />
    </router-link>
    <div class="p-3">
      <h3 class="p-3 font-bold">{{ meal.strMeal }}</h3>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis, saepe!
      </p>
      <div class="flex items-center mt-5 justify-between">
        <YoutubeButton :href="meal.strYoutube"> Youtube</YoutubeButton>
      </div>
    </div>
  </div>
</template>

<script setup>
import YoutubeButton from "./YoutubeButton.vue";

const { meal } = defineProps({
  meal: Object,
});
</script>
