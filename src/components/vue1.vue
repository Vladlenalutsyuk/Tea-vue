<template> 
    <div>
        <button @click="showSquare(2)">Показать квадрат 2</button>
        <button @click="showSquare(3)">Показать квадрат 3</button>
    </div>
</template>

<script>
export default {
    methods: {
        showSquare: function(num) {
            alert(this.calculateSquare(num));
        },
        calculateSquare: function(num) {
            return num * num;
        }
    }
};
</script>
