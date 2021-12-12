<script>
import { Link } from '@inertiajs/inertia-vue3'
import { defineComponent, onMounted, reactive, ref, watch } from 'vue'
/* import _ from 'lodash' */

	export default defineComponent({
		components: {
			Link	
		},
		props: {
			employees: Object,
		},
		setup(props) {
			console.log(props.employees)
			const state = reactive({
				/* employees: Array, */
				newEmployee: Array,
				openModal: Boolean,
			})

			const page = ref(0)

			function next() {
				props.employees.current_page++
			}

			/* onMounted(() => { */
			/* }) */

			/* watch(() => _.cloneDeep([page.value, limit.value]),(currentValue, oldValue) => { */
			/* 	getEmployees() */
			/*   } */
			/* ) */
			
			return {  state, props, page, next }
		}
	}) 		
</script>

<template>
	<div class="min-w-full flex flex-col justify-center mb-8">
		<h1 class="text-2xl mx-4 mt-8">
			<p class="hover:text-blue-400">joetwebdev API</p>
			<p class="text-sm">Laravel Backend</p>
		</h1>

		<table class="max-w-full border rounded-xl divide-y divide-gray-200 mx-4 my-8">
		  <thead>
			<tr>
			  <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">ID</th>
			  <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">User Name</th>
			  <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Name</th>
			  <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Email</th>
			  <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Department</th>
			  <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">City</th>
			  <th class="px-3 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">State</th>
			</tr>
		  </thead>
		  <tbody class="bg-white divide-y divide-gray-200">
			<tr v-for="employee in props.employees.data" :key="employee.id" class="cursor-pointer">
			  <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{{employee.id}}</td>
			  <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{{employee.user_name}}</td>
			  <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{{`${employee.first_name} ${employee.last_name}`}}</td>
			  <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{{employee.email}}</td>
			  <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{{employee.department}}</td>
			  <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{{employee.city}}</td>
			  <td class="px-3 py-4 whitespace-nowrap text-sm text-gray-500">{{employee.state}}</td>
			</tr>
		  </tbody>
		</table>
		<div class="flex justify-between mx-8">
			<Link :href="employees.prev_page_url" class="px-6 py-2 hover:bg-gray-200 rounded-xl">Previous</Link>
			<Link :href="props.employees.next_page_url" class="px-6 py-2 hover:bg-gray-200 rounded-xl">Next</Link>
		</div>
	</div>
</template>
