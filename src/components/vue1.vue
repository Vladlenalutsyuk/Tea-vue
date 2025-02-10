<template>
    <div>
        <button @click="showCurrentDay">Показать текущий день</button>
    </div>
</template>

<script>
export default {
    methods: {
        showCurrentDay: function() {
            let weekday = this.cape(this.getCurrentWeekday());
            alert(weekday);
        },
        cape: function(str) {
            return str[0].toUpperCase() + str.slice(1);
        },
        getCurrentWeekday: function() {
            let days = ["воскресенье", "понедельник", "вторник", "среда", "четверг", "пятница", "суббота"];
            let today = new Date().getDay();
            return days[today] || "Неверное значение";
        }
    }
};
</script>
