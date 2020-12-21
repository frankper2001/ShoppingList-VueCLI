<template>
	<div class="accordion" id="accordion">
		<div class="card card-pendientes">
			<div class="card-header text-white py-0 pl-2 mb-2" id="headingOne">
				<h2 class="mt-2">Pending</h2>
				<button
					class="btn btn-sm btn-link"
					data-toggle="collapse"
					data-target="#collapseOne"
					aria-expanded="true"
					aria-controls="collapseOne"
				>
					<i class="material-icons mt-1">menu</i>
				</button>
			</div>
			<!-- Al tratar de ocultar el bloque "pendiente", solo se oculta la 1ra tarea. Pendiente de corregir -->
			<div
				id="collapseOne"
				class="collapse show align-items-center py-0"
				aria-labelledby="headingOne"
				data-parent="#accordion"
				v-for="(tarea, index) in tareas"
				:key="index"
			>
				<div class="card-body mr-auto">
					<h5 class="float-left pl-1">{{ tarea.tarea }}</h5>
				</div>
				<div>
					<i class="material-icons mr-1">create</i>
					<i class="material-icons mr-2">delete</i>
				</div>
			</div>
		</div>

		<div class="card card-proceso">
			<div class="card-header text-white py-0 pl-2 mb-2" id="headingTwo">
				<h2 class="mt-2">In Progress</h2>

				<button
					class="btn btn-sm btn-link collapsed"
					data-toggle="collapse"
					data-target="#collapseTwo"
					aria-expanded="false"
					aria-controls="collapseTwo"
				>
					<i class="material-icons mt-1">menu</i>
				</button>
			</div>
			<div
				id="collapseTwo"
				class="collapse show align-items-center py-0"
				aria-labelledby="headingTwo"
				data-parent="#accordion"
			>
				<div class="card-body mr-auto">
					<h5 class="float-left pl-1">Item 2</h5>
				</div>
				<div>
					<i class="material-icons mr-1">create</i>
					<i class="material-icons mr-1">delete</i>
				</div>
			</div>
		</div>

		<div class="card card-completadas mb-5">
			<div class="card-header text-white py-0 pl-2 mb-2" id="headingThree">
				<h2 class="mt-2">Completed</h2>

				<button
					class="btn btn-sm btn-link collapsed"
					data-toggle="collapse"
					data-target="#collapseThree"
					aria-expanded="false"
					aria-controls="collapseThree"
				>
					<i class="material-icons mt-1">menu</i>
				</button>
			</div>
			<div
				id="collapseThree"
				class="collapse show align-items-center py-0"
				aria-labelledby="headingThree"
				data-parent="#accordion"
			>
				<div class="card-body mr-auto">
					<h5 class="float-left pl-1">Item 3</h5>
				</div>
				<div>
					<i class="material-icons mr-1">create</i>
					<i class="material-icons mr-1">delete</i>
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
					{ tarea: 'producto 01' },
					{ tarea: 'producto 02' },
					{ tarea: 'producto 03' },
					{ tarea: 'producto 04' },
					{ tarea: 'producto 05' },
					{ tarea: 'producto 06' },
				],
			};
		},
		methods: {},
	};
</script>

<style scoped></style>
