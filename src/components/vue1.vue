<template>
	<ul>
		<li v-for="(item, index) in items" :key="item" @click="removeItem(index)">
			{{ item }}
		</li>
	</ul>
</template>

<script>
import { ref } from "vue";

export default {
	setup() {
		const items = ref(["a", "b", "c", "d", "e"]);

		const removeItem = (index) => {
			items.value = items.value.filter((_, i) => i !== index);
		};

		return { items, removeItem };
	},
};
</script>

<style scoped>
li {
	cursor: pointer;
	user-select: none;
	transition: opacity 0.2s ease-in-out;
}
li:hover {
	opacity: 0.6;
}
</style>
