<template>
	<v-app>
		<v-main>
			<Header></Header>
			<InputField></InputField>
		</v-main>
	</v-app>
</template>

<script>
	import Header from './components/shared/Header.vue';
	import InputField from './components/liveEditor/InputField.vue';

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
