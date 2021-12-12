<script>
import Navbar from './components/Navbar.vue'
import Home from './main/Home.vue'
import About from './main/About.vue'
import Stack from './main/Stack.vue'

import { defineComponent } from 'vue'
export default defineComponent ({
	components: {
		Navbar,
		Home,
		About,
		Stack
	},
})
</script>


<template>
	<header>
		<Navbar />
	</header>
	<main class="flex flex-col justify-center snap-mandatory snap-y">
		<Home />
		<About />
		<Stack />
	</main>
</template>

