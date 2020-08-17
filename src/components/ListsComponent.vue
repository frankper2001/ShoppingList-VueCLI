<template>
	<div>
		<h3>prueba</h3>
		<div class="accordion" id="accordionList">
			<div class="card card-pendientes">
				<div
					class="card-header bg-danger text-white  align-items-center py-0 pl-2"
					id="headingOne"
				>
					<h2 class="mb-0">
						<button
							class="btn btn-sm btn-link"
							type="button"
							data-toggle="collapse"
							data-target="#collapseOne"
							aria-expanded="true"
							aria-controls="collapseOne"
							id="pending"
						>
							Pending
						</button>
					</h2>
					<button
						class="btn btn-sm btn-link"
						type="button"
						data-toggle="collapse"
						data-target="#collapseOne"
						aria-expanded="true"
						aria-controls="collapseOne"
					>
						<i class="material-icons float-right mb-0">menu</i>
					</button>
				</div>
				<div
					id="collapseOne"
					class="collapse show  align-items-center py-0"
					aria-labelledby="headingOne"
					data-parent="#accordionList"
					v-for="item in items"
				>
					<div class="card-body float-left mr-auto pl-2">
						<b>{{item.text}}</b>
					</div>
					<button
						type="button"
						class="btn btn-sm btn-outline-primary float-right mr-2"
					>
						<span class="material-icons">arrow_drop_down</span></button
					><button
						type="button"
						class="btn btn-sm btn-outline-success float-right mr-2"
					>
						<span class="material-icons">arrow_drop_down</span></button
					><i class="material-icons float-right mr-1">create</i
					><i class="material-icons float-right mr-1">delete</i>
				</div>
			</div>

			<div class="card card-proceso"></div>

			<div class="card card-completadas mb-5"></div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'ListComp',
		data() {
			return {
				item: {
					text: ''
				},
				items: [
					{
						text: 'producto 01'
					}
				]
			}
		},
		methods: {
			addItem() {
				let { text } = this.item;
				this.items.push({
					text
				})
			}
		}
	}
</script>

<style scoped></style>
