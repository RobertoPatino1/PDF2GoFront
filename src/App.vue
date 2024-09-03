<template>
	<v-app>
		<v-main>
			<Header></Header>
			<InputField></InputField>
		</v-main>
	</v-app>
</template>

<script>
	import Header from './components/Header.vue';
	import InputField from './components/InputField.vue';

	export default {
		name: 'App',

		components: {
			Header,
			InputField,
		},

		data: () => ({
			//
		}),
	};
</script>
