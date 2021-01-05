<template>
    <form class="form" @submit="changeColor" action="#" method="POST">
        <p class="color-option">Напиши любой текст и выбери ему цвет</p>
        <input class="user-text" type="text" name="color" v-model="text">
        <select class="selection" v-model="color">
            <option v-for="option in options" v-bind:value="option.value">
                {{ option.text }}
            </option>
        </select>
        <button class="btn">Применить цвет</button>
        <div :style="{ color : colorForStyle }"> {{ textFromInput }}</div>
    </form>
</template>

<script>
export default {
    name: "Form2",
    data: function() {
        return {
            color: '#000000',
            text: '',
            textFromInput: null,
            colorForStyle: null,
            options: [
            { text: 'Чёрный', value: '#000000' },
            { text: 'Красный', value: '#ff0000' },
            { text: 'Оранжевый', value: '#ffa500' },
            { text: 'Желтый', value: '#ffff00' },
            { text: 'Зелёный', value: '#008000' },
            { text: 'Голубой', value: '#9ddaff' },
            { text: 'Синий', value: '#0000ff' },
            { text: 'Фиолетовый', value: '#4b0082' }
            ]
        }
    },
    methods: {
        changeColor(e) {
            e.preventDefault();
            this.textFromInput = this.text;
            this.colorForStyle = this.color;
        }
    }
}
</script>

<style scoped lang="scss">
.form {
    height: 200px;
}
.color-option {
    font-size: 20px;
}
.user-text {
    width: 400px;
    height: 30px;
    margin: 20px;
}
.selection {
    width: 120px;
    height: 25px;
    margin: 20px;
    background-color: rgb(223, 233, 248);
}
.btn {
    text-transform: uppercase;
    color: #000000;
    background-color: #d37171;
    border-style: none;
    width: 195px;
    height: 40px;
    margin: 10px 0;
    cursor: pointer;
    transition: all 0.5s ease;
    &:hover {
            background-color: rgb(142, 125, 190);
            color: #ffffff;
      }
}
</style>