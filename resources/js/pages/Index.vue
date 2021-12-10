<script>
/* import NavBar from '../components/NavBar.vue' */
import Home from './main/Home.vue'
import About from './main/About.vue'
import Stack from './main/Stack.vue'

import { defineComponent } from 'vue'
export default defineComponent ({
	components: {
		/* NavBar, */
		Home,
		About,
		Stack
	},
})
</script>


<template>
	<header>
		<!-- <NavBar /> -->
	</header>
	<main class="flex flex-col justify-center bg-gray-600">
		<Home />
		<About />
		<Stack />
	</main>
</template>

