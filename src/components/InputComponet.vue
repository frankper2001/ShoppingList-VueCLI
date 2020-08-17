<template>
	<div>
		<form id="formulario">
			<input
				type="text"
				id="add-tarea"
				autocomplete="off"
				class="form-control form-control-sm my-3"
				placeholder="Write your Item here..."
				
			/>
			<div id="headButtons">
				<button
					type="submit"
					class="btn btn-danger btn-sm mb-3 addToPending"
					id="addToPending"
				>
					Add to Pending
				</button>
				<button
					type="submit"
					class="btn btn-primary btn-sm mb-3 addToInProgress"
					id="addToInProgress"
				>
					Add to In progress
				</button>
				<button
					type="button"
					class="btn btn-warning btn-sm mb-3 clearCompleted"
					id="clearCompleted"
				>
					Clear completed
				</button>
				<button
					type="button"
					class="btn btn-warning btn-sm mb-3 clearAll"
					id="clearAll"
				>
					Clear All
				</button>
			</div>
		</form>
	</div>
</template>

<script>
	export default {
		name: 'InputComp'
	};
</script>

<style scoped></style>
