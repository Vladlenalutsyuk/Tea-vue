<script>
export default {
	data() {
		return {
			name: "Иван Иванов",
			position: "Разработчик",
			salary: 100000,
		};
	},
};
</script>

<template>
	<div class="employee-card">
		<h3>{{ name }}</h3>
		<p>Должность: {{ position }}</p>
		<p>Зарплата: {{ salary }} ₽</p>
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
h3 {
	color: #333;
}
p {
	margin: 5px 0;
}
</style>
