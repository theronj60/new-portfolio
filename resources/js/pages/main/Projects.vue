<script>
	import { defineComponent } from 'vue'
	/* import stackBackImg from '../assets/antelope.jpeg' */
	export default defineComponent({
		setup() {
			/* const bgImg = `background-image: url(${stackBackImg}); background-size: cover;` */
			return {  }
		}
	})
</script>
<template>
	<section id="stack" class="min-h-screen flex items-center justify-center" :style="bgImg">
		<div class="text-2xl text-white">
			project page
		</div>
	</section>
</template>
