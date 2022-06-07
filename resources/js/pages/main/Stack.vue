<script>
	import { defineComponent } from 'vue'
	import stackBackImg from '/imgs/antelope.jpeg'
	export default defineComponent({
		setup() {
			const bgImg = `background-image: url(${stackBackImg}); background-size: cover;`
			const foo = 'bar'
			return { foo, bgImg }
		}
	})
</script>
<template>
	<section id="stack" class="min-h-screen flex items-center justify-center" :style="bgImg">
		<div class="grid grid-cols-4 space-x-4 space-y-k items-center text-2xl text-white">
			<div class="flex flex-col items-center justify-center border-2 bg-gray-700 bg-opacity-50 p-2 rounded-xl shadow">
				<div class="bg-black rounded h-16 w-16">
					<!-- will hold image -->
				</div>
				<div>
					Neovim
				</div>
				<span class="text-sm">My preferred editor of choice.</span>
			</div>
			<div class="flex border-2 bg-gray-700 bg-opacity-50 rounded-xl shadow">
				Vue 2/3
			</div>
			<div class="flex border-2 bg-gray-700 bg-opacity-50 rounded-xl shadow">
				Laravel
			</div>
			<div class="flex border-2 bg-gray-700 bg-opacity-50 rounded-xl shadow">
				Tailwind CSS
			</div>
		</div>
	</section>
</template>
