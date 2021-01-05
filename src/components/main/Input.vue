<template>
    <form @submit="notSubmit" action="#" method="POST">
        <p class="pick-number">Введите число</p>
        <button class="btn-decr" v-on:click="--total" v-bind:disabled="total < 1">-</button>
        <button class="btn-incr" v-on:click="++total">+</button>
        <p>{{ total }}</p>
        <input type="number" class="input" v-model.number="number" @blur="changeNumber">
    </form>
</template>

<script>
    export default {
        name: "number",
        data: function() {
            return {
                number: '',
                total: ''
            }
        },
        methods: {
            changeNumber() {
                this.total = this.number;
                this.number = '';
            },
            notSubmit(e) {
                e.preventDefault();
            }
        },

    }
</script>

<style scoped lang="scss">
    .pick-number {
        font-size: 20px;
    }
    button {
        text-transform: uppercase;
        color: #000000;
        background-color: #87acd6;
        border: 1px solid black;
        width: 70px;
        height: 40px;
        margin: 10px;
        cursor: pointer;
        transition: all 0.5s ease;
        &:hover {
            background-color: rgb(130, 179, 174);
            color: #ffffff;
        }
    }
</style>