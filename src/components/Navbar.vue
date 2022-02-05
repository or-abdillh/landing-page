<template>
	<main class="navbar">
		<section class="navbar-brand">
			<img src="/logo.png" width="45" />
			<h1 class="text-gray-50 text-xl font-semibold lg:text-3xl">HIMA TI POLIHASNUR</h1>
			<button @click="showMenu = true" class="active:scale-95 duration-300 lg:hidden" type="button">
				<i class="fa fa-bars text-gray-50 text-2xl"></i>
			</button>
		</section>

		<section :class="showMenu ? 'right-0' : '-right-full'" class="navbar-menu">
			<ul class="navbar-list">
			<span @click="showMenu = false"><i class="fa fa-times lg:hidden text-gray-50"></i></span>
				<template v-for="(menu, x) in menus" :key="x">
					<li :class="menuActive === menu.name ? 'border-b-4 border-blue-400' : ''" class="text-gray-50 font-medium">{{ menu.name }}</li>
				</template>
			</ul>
		</section>
	</main>
</template>

<style scoped>
	.navbar {
		@apply z-20 lg:flex lg:items-center lg:justify-between lg:px-10 w-full bg-gradient-to-r from-sky-500 to-indigo-600 fixed top-0 left-0 right-0 px-5 lg:py-8 py-3;
	}

	.navbar-brand {
		@apply flex items-center justify-between lg:gap-3;
	}

	.navbar-menu {
		@apply duration-300 fixed lg:relative top-0 bottom-0 bg-blue-600 lg:bg-opacity-0 px-5 lg:px-0 pt-12 lg:pt-0;
	}

	.navbar-list {
		@apply flex flex-col lg:flex-row gap-3 lg:gap-10 lg:text-xl;
	}
</style>

<script setup>

	import { ref, computed } from 'vue'

	const menuActive = ref('Beranda')
	const showMenu = ref(false)
	const viewport = computed(() => window.innerWidth)

	if ( viewport.value > 1000 ) showMenu.value = true
	
	const menus = [
		{
			name: 'Beranda',
			to: '#'
		},
		{
			name: 'Tentang',
			to: '#'
		},
		{
			name: 'Kegiatan',
			to: '#'
		},
		{
			name: 'FAQ',
			to: '#'
		},
		{
			name: 'Narahubung',
			to: '#'
		}
	]
	
</script>
