<template>
    <form class="form" @submit="changeColor" action="#" method="POST">
        <p class="color-option">Напиши название цвета (eng)</p>
        <input class="user-text" type="text" name="color" v-model="textColor">
        <button class="btn">Применить цвет</button>
        <div :style="{ color : colorAsStyle }"> {{ colorAsStyle }}</div>
    </form>
</template>

<script>
export default {
    name: "Form",
    data: function () {
        return {
            textColor: '',
            colorAsStyle: null,
        }
    },
    methods: {
        changeColor(e) {
            e.preventDefault();
            this.colorAsStyle = this.textColor;
        }
    }
}
</script>

<style scoped lang="scss">
.form {
    height: 250px;
}
.color-option {
    font-size: 30px;
}
.user-text {
    width: 200px;
    height: 30px;
    margin: 20px;
}
.btn {
    text-transform: uppercase;
    color: #000000;
    background-color: #c796b7;
    border-style: none;
    width: 195px;
    height: 40px;
    margin: 10px 0;
    cursor: pointer;
    transition: all 0.5s ease;
    &:hover {
            background-color: rgb(150, 65, 105);
            color: #ffffff;
      }
}
</style>