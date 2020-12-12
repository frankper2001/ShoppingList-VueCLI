<template>
	<div>
		<div class="accordion" id="accordionList">
			<div class="card card-pendientes">
				<div class="card-header bg-danger text-white py-0 pl-2" id="headingOne">
					<h2 class="mt-2">Pending</h2>

					<button
						class="btn btn-sm btn-link"
						type="button"
						data-toggle="collapse"
						data-target="#collapseOne"
						aria-expanded="true"
						aria-controls="collapseOne"
					>
						<i class="material-icons mt-1">menu</i>
					</button>
				</div>
				<div
					id="collapseOne"
					class="collapse show align-items-center py-0"
					aria-labelledby="headingOne"
					data-parent="#accordionList"
					v-for="(tarea, index) in tareas"
					:key="index"
				>
					<div class="card-body mr-auto">
						<h5 class="float-left pl-1">{{ index + 1 }}</h5>
						<h3 class="float-left pl-1">{{ tarea.tarea }}</h3>
						<h5 class="float-left pl-1">{{ tarea.date }}</h5>
					</div>
					<div>
						<i class="material-icons">arrow_drop_down</i>
						<i class="material-icons">arrow_drop_down</i>
						<i class="material-icons mr-1">create</i>
						<i class="material-icons mr-1">delete</i>
					</div>
				</div>
			</div>

			<div class="card card-proceso">
				<div
					class="card-header bg-primary text-white py-0 pl-2"
					id="headingTwo"
				>
					<h2 class="mt-2">In Progress</h2>

					<button
						class="btn btn-sm btn-link"
						type="button"
						data-toggle="collapse"
						data-target="#collapseTwo"
						aria-expanded="true"
						aria-controls="collapseTwo"
					>
						<i class="material-icons mt-1">menu</i>
					</button>
				</div>
				<div
					id="collapseTwo"
					class="collapse show align-items-center py-0"
					aria-labelledby="headingTwo"
					data-parent="#accordionList"
				>
					<div class="card-body mr-auto">
						<h3 class="float-left pl-1">Item 2</h3>
					</div>
					<div>
						<i class="material-icons">arrow_drop_down</i>
						<i class="material-icons">arrow_drop_down</i>
						<i class="material-icons mr-1">create</i>
						<i class="material-icons mr-1">delete</i>
					</div>
				</div>
			</div>

			<div class="card card-completadas mb-5">
				<div
					class="card-header bg-success text-white py-0 pl-2"
					id="headingThree"
				>
					<h2 class="mt-2">Completed</h2>

					<button
						class="btn btn-sm btn-link"
						type="button"
						data-toggle="collapse"
						data-target="#collapseThree"
						aria-expanded="true"
						aria-controls="collapseThree"
					>
						<i class="material-icons mt-1">menu</i>
					</button>
				</div>
				<div
					id="collapseThree"
					class="collapse show align-items-center py-0"
					aria-labelledby="headingThree"
					data-parent="#accordionList"
				>
					<div class="card-body mr-auto">
						<h3 class="float-left pl-1">Item 3</h3>
					</div>
					<div>
						<i class="material-icons">arrow_drop_down</i>
						<i class="material-icons">arrow_drop_down</i>
						<i class="material-icons mr-1">create</i>
						<i class="material-icons mr-1">delete</i>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'ListComp',
		data() {
			return {
				tareas: [
					{ tarea: 'producto 01', date: '' },
					{ tarea: 'producto 02', date: '' },
					{ tarea: 'producto 03', date: '' },
					{ tarea: 'producto 04', date: '' },
					{ tarea: 'producto 05', date: '' },
					{ tarea: 'producto 06', date: '' },
				],
			};
		},
		methods: {},
	};
</script>

<style scoped></style>
