<script>
import { Link } from '@inertiajs/inertia-vue3'
import { defineComponent, reactive } from 'vue'
/* import _ from 'lodash' */

	export default defineComponent({
		components: {
			Link	
		},
		props: {
			employee: Object,
		},
		setup(props) {
			console.log(props.employees)
			const state = reactive({
				openModal: Boolean,
			})

			/* onMounted(() => { */
			/* }) */

			/* watch(() => _.cloneDeep([page.value, limit.value]),(currentValue, oldValue) => { */
			/* 	getEmployees() */
			/*   } */
			/* ) */
			
			return {  state, props }
		}
	}) 		
</script>

<template>
	<div class="flex flex-col justify-center mb-8 mx-4">
		<h1 class="text-2xl mx-4 mt-8">
			<p class="">Show Employee</p>
		</h1>
		<div class="flex justify-end mx-4">
			<button class="px-6 bg-gray-400 text-white py-2 rounded-xl">Edit</button>
		</div>
		<div class="flex space-x-8 mx-4">
			<span class="flex flex-col">
				<label for="first-name">First Name</label>
				<input type="text" v-model="employee.first_name" name="first-name" id="" class="outline-none border p-2 rounded" />
			</span>
			<span class="flex flex-col">
				<label for="last-name">Last Name</label>
				<input type="text" v-model="employee.last_name" name="last-name" id="" class="outline-none border p-2 rounded"/>
			</span>
		</div>
		<div class="flex justify-end mx-4">
			<button class="px-6 bg-green-400 text-white py-2 rounded-xl">Save</button>
		</div>
	</div>
</template>
