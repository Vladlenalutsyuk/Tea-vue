<script>
export default {
    data() {
	return {
		obj: {x: 1, y: 2, z: 3},
	}
},
methods: {
	show: function() {
		alert(new Date());
	}
}
}

</script>
<template>
	<div>
		
		{{ show() }}
	</div>
</template>