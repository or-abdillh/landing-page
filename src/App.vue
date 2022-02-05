<template>
	<Navbar />
	<main class="w-full">

		<section class="lg:min-h-screen section bg-gradient-to-r from-sky-500 to-indigo-600">
			<Headline />
		</section>

		<section class="section bg-gray-100">
			<About />
		</section>
		
	</main>
</template>

<script setup>

	import Navbar from '@/components/Navbar.vue'
	import Headline from '@/components/Headline.vue'
	import About from '@/components/About.vue'

</script>

<style scoped>
	.section {
		@apply w-full px-6 py-8 md:px-16 xl:px-28;
	}
</style>
