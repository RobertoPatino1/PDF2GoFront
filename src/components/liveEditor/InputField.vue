<template>
	<v-container fluid>
		<div class="textarea-container">
			<div class="line-numbers">
				<pre>{{ lineNumbers }}</pre>
			</div>
			<v-textarea
				v-model="value"
				:rules="rules"
				clear-icon="mdi-close-circle"
				bg-color="grey-lighten-2"
				color="basil"
				variant="solo-filled"
				@input="updateLineNumbers"
			></v-textarea>
		</div>
	</v-container>
</template>

<script setup>
	import { ref } from 'vue';

	const value = ref('# Hello World!\n');
	const lineNumbers = ref('1');

	function updateLineNumbers() {
		const lines = value.value.split('\n').length;
		lineNumbers.value = Array.from({ length: lines }, (_, i) => i + 1).join(
			'\n'
		);
	}
</script>

<style scoped>
	.textarea-container {
		display: flex;
		position: relative;
	}

	.line-numbers {
		padding: 16px;
		background-color: #f4f4f4;
		text-align: right;
		user-select: none;
		font-family: monospace;
		font-size: large;
		color: #aaa;
	}

	v-textarea {
		flex: 1;
		font-family: monospace;
	}
</style>
