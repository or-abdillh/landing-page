<template>
	<main>
		<h1 class="text-center pb-6 text-3xl md:text-4xl lg:text-5xl font-semibold text-indigo-500">Pengumuman</h1>
		<p class="text-gray-600 text-center lg:px-24">Update terkini tentang IT Gatehring HIMA TI Tahun 2022 bisa kamu temukan disini</p>

		<section class="mt-10 md:flex flex-wrap justify-between gap-10">
			<template v-for="(feed, x) in announcements" :key="x">
				<FeedList :feed="feed" />
			</template>
		</section>
	</main>
</template>

<script setup>
	import FeedList from '@/components/FeedList.vue'
	import announcements from '@/announcements.js' 
</script>
