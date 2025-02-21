<script>
import Employee from "./components/Employee.vue"; // Импортируем компонент

export default {
	components: {
		Employee, // Регистрируем компонент
	},
};
</script>

<template>
	<div>
		<h2>Список сотрудников</h2>
		<Employee />
		<Employee />
		<Employee />
	</div>
</template>

<style scoped>
h2 {
	text-align: center;
	color: #222;
}
</style>
