<template>
	<ul>
		<li><a href="#">Home</a></li>
		<li><a href="#">Projetos</a></li>
		<li><a href="#">Contato</a></li>
	</ul>
</template>

<script>
export default {
	name: 'Header',
};
</script>

<style scoped>
ul {
	list-style: none;
	display: flex;
	background-color: gray;
	padding: 1rem;
}

li {
	margin-right: 10px;
}

a {
	color: black;
	text-decoration: none;
	transition: 0.5s;
}

a:hover {
	color: rgb(43, 226, 214);
}
</style>
