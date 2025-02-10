

<template>
    <div>
		<input v-model.number="num" type="number">
        <button @click="show">click</button>
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
                show: function() {
                    let weekday = this.cape(this.getWeekday(this.num));
					
                    alert(weekday);
                },
				cape: function(str) {
                    return str[0].toUpperCase() + str.slice(1);
                },
                getWeekday: function() {
                    let days = ["воскресенье", "понедельник", "вторник", "среда", "четверг", "пятница", "суббота"];
                    return days[this.num - 1] || "Неверное значение";
                }
            }
        };
</script>