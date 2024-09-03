<template>
	<v-container fluid>
		<v-textarea
			:model-value="value"
			:rules="rules"
			clear-icon="mdi-close-circle"
			bg-color="grey-lighten-2"
			color="basil"
			label="Your Markdown Code"
			mode-value="This is clearable text."
			clearable
			counter
		></v-textarea>
	</v-container>
</template>

<script setup>
	import { ref } from 'vue';
	// TODO: Add a character limit???
	// const rules = [(v) => v.length <= 25 || 'Max 25 characters'];

	const value = ref('# Hello World!\n');
</script>

<script>
	export default {
		data: () => ({
			// rules: [(v) => v.length <= 25 || 'Max 25 characters'],
			value: 'Hello World!',
		}),
	};
</script>
