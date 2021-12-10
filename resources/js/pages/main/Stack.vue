<script>
	import { defineComponent } from 'vue'
	/* import stackBackImg from '../assets/antelope.jpeg' */
	export default defineComponent({
		setup() {
			/* const bgImg = `background-image: url(${stackBackImg}); background-size: cover;` */
			const foo = 'bar'
			return { foo }
		}
	})
</script>
<template>
	<section id="stack" class="min-h-screen flex items-center justify-center" :style="bgImg">
		<div class="text-2xl text-white">
			Software, Text Editors, Frameworks
		</div>
	</section>
</template>
