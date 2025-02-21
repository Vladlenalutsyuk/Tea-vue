<script>
export default {
	props: {
		name: String,
		surname: String,
		age: Number,
	},
};
</script>

<template>
	<div class="employee-card">
		<p><strong>Имя:</strong> {{ name }}</p>
		<p><strong>Фамилия:</strong> {{ surname }}</p>
		<p><strong>Возраст:</strong> {{ age }} лет</p>
	</div>
</template>

<style scoped>
.employee-card {
	border: 1px solid #ddd;
	padding: 15px;
	margin: 10px;
	border-radius: 8px;
	box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
	background: #f9f9f9;
}
p {
	font-size: 16px;
}
strong {
	color: #333;
}
</style>
