<script setup>
const props = defineProps({
    meal: {
        required: true,
        type: Object
    }
})
</script>

<template>
    <div class="bg-white shadow rounded-xl">
        <router-link :to="`/meal/${props.meal.idMeal}`">
            <img :src="props.meal.strMealThumb" class="rounded-t-xl h-48 object-cover w-full"/>
        </router-link>
        <div class="p-3">
            <h3 class="font-bold">{{ props.meal.strMeal }}</h3>
            <p class="mb-4 line-clamp-3">{{ props.meal.strInstructions }}</p>
        </div>
    </div>
</template>