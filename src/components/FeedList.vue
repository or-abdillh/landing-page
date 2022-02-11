<script setup>
  //For render announcment content
	const props = defineProps({
		feed: {
			type: Object
		}
	})	
</script>

<template>
	<main class="w-full md:w-5/12 mb-10 md:mb-0 border-b-2 pb-6">
		<section>
			<h1 class="mb-2 md:mb-4 text-lg font-medium text-indigo-600">{{ feed.title }}</h1>
			<small class="text-indigo-600 font-medium">{{ feed.publishDate }}</small>
			<p v-html="feed.content" class="text-gray-700 text-sm"></p>
		</section>
	</main>
</template>
