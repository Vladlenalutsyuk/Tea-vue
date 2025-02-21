<script>
import Employee from "./components/Employee.vue"; // Импортируем компонент

export default {
	data() {
		return {
			employees: [
				{ id: 1, name: "Иван", surname: "Иванов", age: 30 },
				{ id: 2, name: "Анна", surname: "Петрова", age: 25 },
				{ id: 3, name: "Сергей", surname: "Сидоров", age: 40 },
			],
		};
	},
	components: {
		Employee,
	},
};
</script>

<template>
	<div>
		<h2>Список сотрудников</h2>
		<Employee
			v-for="employee in employees"
			:key="employee.id"
			:name="employee.name"
			:surname="employee.surname"
			:age="employee.age"
		/>
	</div>
</template>

<style scoped>
h2 {
	text-align: center;
	color: #222;
}
</style>
