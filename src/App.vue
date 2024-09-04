<template>
	<v-app>
		<v-main>
			<Header :activeTab="tab" @update:activeTab="tab = $event" />
			<LiveEditorPanel v-if="tab === 'Live Editor'" />
			<!-- TODO: Add upload document panel -->
		</v-main>
	</v-app>
</template>

<script>
	import Header from './components/shared/Header.vue';
	import Panels from './components/liveEditor/LiveEditorPanel.vue';
	import { ref } from 'vue';
	import LiveEditorPanel from './components/liveEditor/LiveEditorPanel.vue';

	export default {
		name: 'App',
		components: {
			Header,
			Panels,
		},
		setup() {
			const tab = ref('Live Editor'); // Valor inicial para la pestaña activa
			return { tab };
		},
	};
</script>
