<template>
	<table>
		<thead>
			<tr>
				<th>ID</th>
				<th>Имя</th>
				<th>Зарплата</th>
				<th>Возраст</th>
				<th>Действия</th>
			</tr>
		</thead>
		<tbody>
			<tr v-for="user in users" :key="user.id">
				<td>{{ user.id }}</td>
				<td>{{ user.name }}</td>
				<td>{{ user.salary }}</td>
				<td>{{ user.age }}</td>
				<td>
					<a href="#" @click.prevent="removeUser(user.id)">Удалить</a>
				</td>
			</tr>
		</tbody>
	</table>
</template>

<script>
import { ref } from "vue";

export default {
	setup() {
		const users = ref([
			{ id: 1, name: "name1", salary: 100, age: 30 },
			{ id: 2, name: "name2", salary: 200, age: 40 },
			{ id: 3, name: "name3", salary: 300, age: 50 },
		]);

		const removeUser = (id) => {
			users.value = users.value.filter((user) => user.id !== id);
		};

		return { users, removeUser };
	},
};
</script>

<style scoped>
table {
	width: 100%;
	border-collapse: collapse;
	margin-top: 20px;
}

th, td {
	border: 1px solid #ddd;
	padding: 8px;
	text-align: left;
}

th {
	background-color: #f4f4f4;
}

a {
	color: red;
	cursor: pointer;
	text-decoration: none;
}

a:hover {
	text-decoration: underline;
}
</style>
