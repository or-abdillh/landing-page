<template>
	<main class="mb-10">
		<section class="w-full flex items-center justify-between">
			<strong class="w-8/12 text-gray-700">1. Apakah harus ada biaya yanng dibayarkan sebagai peserta ?</strong>
			<i @click="showElement = !showElement" :class="showElement ? 'fa-minus' : 'fa-plus'" class="active:scale-95 fa text-indigo-600"></i>
		</section>
		<section v-if="showElement" class="mt-3 duration-300 border-b-2 pb-4">
			<p class="text-gray-600">Dalam kegiatan ini para peserta diwajibkan membayar iuran sebesar Rp20.000 per orang dan hanya dibayar satu kali selama berkegiatan</p>
		</section>
	</main>
</template>
<script setup>
	import { ref } from 'vue'

	const showElement = ref(false)
</script>
