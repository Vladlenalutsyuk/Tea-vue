<script>
export default {
    data() {
        return {
            obj: { x: 1, y: 2, z: 3 },
        };
    },
    methods: {
        show() {
            alert(new Date());
        }
    }
};
</script>

<template>
    <div>
        <button @mouseover="show">date</button>
    </div>
</template>
