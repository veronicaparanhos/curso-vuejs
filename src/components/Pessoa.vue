<template>
	<div>
		<h2>Está é a descrição da pessoa: {{ nome }}</h2>
		<info />
		<Form />
	</div>
</template>

<script>
import Info from './Info.vue';
import Form from './Form.vue';

export default {
	components: { Info, Form },
	name: 'Pessoa',
	data() {
		return {
			nome: 'Verônica',
		};
	},
};
</script>
