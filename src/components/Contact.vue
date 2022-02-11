<template>
	<main>
		<h1 class="text-center pb-6 text-3xl md:text-4xl lg:text-5xl font-semibold text-indigo-500">Narahubung</h1>
		<p class="text-gray-600 text-center lg:px-24">Masih perlu ada yang ditanyakan ? silahkan menghubungi kontak narahubung kami dibawah ini</p>
		<section class="mt-12 md:flex justify-evenly gap-6">
			<template v-for="(contact, x) in contacts" :key="x">
				<CardProfile :useSosmed="false" :profile="contact">
					<template v-slot:footer>
						<a class="active:ring-2 ring-gray-100 duration-300 w-8/12 mx-auto mt-4 block bg-gradient-to-r from-green-400 to-green-600 text-center py-2 rounded-xl text-gray-50 font-medium text-base" :href="createLink(contact.contact)">
							<i class="fab fa-whatsapp"></i>
							contact me
						</a>
					</template>
				</CardProfile>
			</template>
		</section>
	</main>
</template>

<script setup>
	import contacts from '@/contacts.js'
	import CardProfile from '@/components/CardProfile.vue'
  
  //Generate link to api.whatsapp
	const createLink = num => `https://api.whatsapp.com/send?phone=${num}`
</script>
