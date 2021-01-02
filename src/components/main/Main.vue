<template>
  <div class="container" id="main-block">
    <button class="btn" v-on:click="hello">Плюсуем числа</button>
    <ul class="num">
      <li>{{numbers}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Main",
  props: {
    numbers: []
  },
  methods: {
    hello() {
        if (!this.numbers) {
            this.numbers = Math.random();
        } else {
            this.numbers += Math.random();
        }
      
    }
  }
 
};
</script>

<style scoped lang="scss">
#main-block {
    height: 150px;
}
.btn {
    display: block;
    margin: 100px auto 20px;
    text-transform: uppercase;
    color: #000000;
    background-color: #976262;
    border-style: none;
    width: 195px;
    height: 50px;
    cursor: pointer;
    transition: all 0.5s ease;
    &:hover {
            background-color: rgb(138, 130, 212);
            color: #ffffff;
      }
}
.num {
    list-style: none;
    padding: 0;
}
</style>
    
