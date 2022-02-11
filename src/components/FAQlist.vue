<template>
	<main class="mb-10">
		<section class="w-full flex items-center justify-between">
			<strong class="w-8/12 text-gray-700">{{ list.num }}. {{ list.question }}</strong>
			<i @click="showElement = !showElement" :class="showElement ? 'fa-minus' : 'fa-plus'" class="active:scale-90 duration-300 fa text-indigo-600"></i>
		</section>
		<section v-if="showElement" class="mt-3 duration-300 border-b-2 pb-4">
			<p class="text-gray-600">{{ list.answer }}</p>
		</section>
	</main>
</template>
<script setup>
	import { ref } from 'vue'
  
  //Handler for expand content
	const showElement = ref(false)
	const props = defineProps({
		list: {
			type: Object
		}
	})
</script>
