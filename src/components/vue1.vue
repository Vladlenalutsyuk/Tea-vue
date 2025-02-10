<template> 
    <div>
        <input v-model.number="num" type="number" placeholder="Введите число">
        <button @click="showSquare">Показать квадрат числа</button>
    </div>
</template>

<script>
export default {
    data() {
        return {
            num: null,
        };
    },
    methods: {
        showSquare: function() {
            if (this.num !== null) {
                alert(this.calculateSquare(this.num));
            } else {
                alert("Введите число");
            }
        },
        calculateSquare: function(num) {
            return num * num;
        }
    }
};
</script>
