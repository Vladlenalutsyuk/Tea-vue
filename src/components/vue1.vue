<script>
export default {
    data() {
	return {
		text: 'page',
		href: 'page.html',
	}
}
}
</script>
<template>
	<div>
		<a :href="href">page</a>
	</div>
</template>