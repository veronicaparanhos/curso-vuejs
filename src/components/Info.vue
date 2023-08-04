<template>
	<div>
		<p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
		<p v-else>Não estou trabalhando no momento</p>
		<p>Utilizo as seguintes tecnologias para back-end:</p>
		<ul>
			<li v-for="(tecnology, index) in backend_tech" :key="index">
				{{ tecnology }}
			</li>
		</ul>
		<p>Utilizo as seguintes tecnologias para o front-end:</p>
		<ul>
			<li v-for="tecnology in frontend_tech" :key="tecnology.id">
				{{ tecnology.language }}
			</li>
		</ul>
		<p v-if="4 > 2">Testando</p>
		<div>
			<button @click="showEmail">{{ texto_botao }}</button>
		</div>
		<p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
		<Picture />
		<p class="teste">
			Para acessar meu portfólio basta clicar
			<a v-bind:href="meu_link" target="_blank">aqui</a>
		</p>
	</div>
</template>

<script>
import Picture from './Picture.vue';
export default {
	name: 'Info',
	components: {
		Picture,
	},
	data() {
		return {
			esta_trabalhando: false,
			mostrar_email: false,
			email: 'veronicahp@gmail.com',
			meu_link: 'http://www.google.com.br',
			texto_botao: 'Mostrar email',
			backend_tech: ['PHP', 'Python', 'Node'],
			frontend_tech: [
				{ id: 1, language: 'HTML' },
				{ id: 2, language: 'CSS' },
				{ id: 3, language: 'JavaScript' },
			],
		};
	},
	methods: {
		showEmail() {
			this.mostrar_email = !this.mostrar_email;
			if (this.mostrar_email) {
				this.texto_botao = 'Esconder email';
			} else {
				this.texto_botao = 'Mostrar email';
			}
		},
	},
};
</script>
