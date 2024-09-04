<template>
	<v-container fluid>
		<v-textarea
			v-model="value"
			:rules="rules"
			clear-icon="mdi-close-circle"
			bg-color="grey-lighten-2"
			color="basil"
			label="Your Markdown Code"
			mode-value="This is clearable text."
			variant="solo-filled"
			prepend-icon="mdi-language-markdown"
		>
			clearable counter ></v-textarea
		>
	</v-container>
</template>

<script setup>
	import { ref } from 'vue';
	// TODO: Add a character limit???
	// const rules = [(v) => v.length <= 25 || 'Max 25 characters'];

	const value = ref('# Hello World!\n');
</script>
