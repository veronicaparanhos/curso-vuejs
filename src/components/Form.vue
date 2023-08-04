<template>
	<div>
		<h2>Meu Formulário:</h2>
		<form action="" @submit="enviarForm($event)">
			<div>
				<InputText />
			</div>
			<div>
				<input type="text" v-model="name" />
				<input type="text" v-model="email" />
			</div>
			<div>
				<Submit />
			</div>
		</form>
		<br />
		<br />
		<br />
	</div>
</template>

<script>
import InputText from './form/InputText.vue';
import Submit from './form/Submit.vue';

export default {
	name: 'Form',
	components: {
		InputText,
		Submit,
	},
	data() {
		return {
			name: '',
			email: '',
		};
	},
	methods: {
		enviarForm(e) {
			e.preventDefault();

			const name = this.name;
			const email = this.email;

			console.log('Formulário enviado!');
			console.log('O nome é: ' + name);
			console.log('O email é: ' + email);

			//Ajax
			//Inserir os dados no banco
		},
	},
};
</script>
