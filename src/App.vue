<template>
	<Navbar />
	<main class="w-full">

		<section class="lg:min-h-screen w-full px-6 py-8 md:px-16 xl:px-28 bg-gradient-to-r from-sky-500 to-indigo-600">
			<Headline />
		</section>
		
	</main>
</template>

<script setup>

	import Navbar from '@/components/Navbar.vue'
	import Headline from '@/components/Headline.vue'
	//clip-path: polygon(100% 0%, 75% 50%, 100% 100%, 25% 100%, 0% 50%, 25% 0%);

</script>
