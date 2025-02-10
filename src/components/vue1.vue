<script>
export default {
    data() {
        return {
			num1: 1,
			num2: 2,
        };
    },
    methods: {
        show() {
            alert(this.num1);
			alert(this.num2);
        }
    }
};
</script>

<template>
    <div>
        <p> {{num1 + num2}}</p>
    </div>
</template>
