<!-- TODO: Make panels take components dynamically -->
<template>
	<v-container class="panels-container" fluid>
		<div class="textarea-wrapper">
			<InputField />
			<InputField />
		</div>
	</v-container>
</template>

<script>
	import InputField from './InputField.vue';

	export default {
		name: 'Panels',
		components: {
			InputField,
		},
	};
</script>

<style scoped>
	.panels-container {
		display: flex;
		justify-content: center; /* Centrar los paneles horizontalmente */
		padding-top: 30px;
	}

	.textarea-wrapper {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 40px; /* Mayor espaciado entre los dos textarea */
		width: 100%; /* Asegurar que el grid tome todo el espacio */
		max-width: 1200px; /* Limitar el ancho total de los paneles */
	}

	textarea {
		height: 500px; /* Hacer los textarea más altos */
		width: 100%; /* Asegurarse de que el textarea ocupe todo el ancho del grid */
	}
</style>
