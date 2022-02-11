<script setup>

	//Props
	const props = defineProps({
		profile: {
			type: Object
		},
		useSosmed: {
			type: Boolean,
			default: true
		}
	})
	
</script>

<template>
	<main class="md:w-4/12 p-6 rounded-xl shadow-lg border-4 border-gray-200 bg-gradient-to-r from-sky-600 to-indigo-700 text-gray-50 mb-6">
		<img :src="profile.avatar" class="rounded-full mx-auto mb-5" width="100" />
		<div class="text-center">
			<h1 class="text-xl font-semibold">{{ profile.name }}</h1>
			<h3 class="md:text-sm">{{ profile.job }}</h3>
		</div>
		<div v-if="useSosmed"  class="w-full flex justify-center gap-3 mt-4">
			<a href="" >
				<i class="fab fa-instagram"></i>
			</a>
			<a href="" >
				<i class="fab fa-facebook"></i>
			</a>
			<a href="" >
				<i class="fab fa-youtube"></i>
			</a>
		</div>

		<slot name="footer"></slot>
		
	</main>
</template>