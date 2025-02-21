<template>
	<table>
		<thead>
			<tr>
				<th>ID</th>
				<th>Имя</th>
				<th>Фамилия</th>
				<th>Действия</th>
			</tr>
		</thead>
		<tbody>
			<tr v-for="user in users" :key="user.id">
				<!-- Обычный режим (не редактирование) -->
				<template v-if="editingUser?.id !== user.id">
					<td>{{ user.id }}</td>
					<td>{{ user.name }}</td>
					<td>{{ user.surn }}</td>
					<td>
						<a href="#" @click.prevent="edit(user)">Редактировать</a> |
						<a href="#" @click.prevent="remove(user.id)">Удалить</a>
					</td>
				</template>

				<!-- Режим редактирования -->
				<template v-else>
					<td>{{ user.id }}</td>
					<td><input v-model="editingUser.name" placeholder="Имя"></td>
					<td><input v-model="editingUser.surn" placeholder="Фамилия"></td>
					<td>
						<a href="#" @click.prevent="save(user)">Сохранить</a> |
						<a href="#" @click.prevent="cancel()">Отмена</a>
					</td>
				</template>
			</tr>
		</tbody>
	</table>
</template>

<script>
import { ref } from "vue";

export default {
	setup() {
		const users = ref([
			{ id: 1, name: "name1", surn: "surn1" },
			{ id: 2, name: "name2", surn: "surn2" },
			{ id: 3, name: "name3", surn: "surn3" },
		]);

		const editingUser = ref(null);
		const originalUser = ref(null);

		const edit = (user) => {
			editingUser.value = { ...user }; // Создаем копию объекта
			originalUser.value = { ...user }; // Сохраняем оригинальные данные
		};

		const save = (user) => {
			Object.assign(user, editingUser.value); // Обновляем объект
			editingUser.value = null; // Выходим из режима редактирования
			originalUser.value = null;
		};

		const cancel = () => {
			editingUser.value = null;
			originalUser.value = null;
		};

		const remove = (id) => {
			users.value = users.value.filter(user => user.id !== id);
		};

		return { users, editingUser, edit, save, cancel, remove };
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
	color: blue;
	cursor: pointer;
	text-decoration: none;
	margin-right: 10px;
}

a:hover {
	text-decoration: underline;
}

input {
	padding: 5px;
}
</style>
