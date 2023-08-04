<template>
	<div>
		<h1>Olá Vue!</h1>
		<p>Meu nome é {{ nome }} e trabalho com {{ profissão }}</p>
	</div>
</template>

<script>
export default {
	name: 'PrimeiroComponente',
	data() {
		return {
			nome: 'Matheus',
			profissão: 'programador',
		};
	},
};
</script>
