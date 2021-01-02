<template>
    <ul class="nav-menu">
        <li class="nav-menu__item" id="menu" v-for="item in items">{{ item }}</li>
        <!-- <li class="nav-menu__item">Head</li>
        <li class="nav-menu__item">Portfolio</li>
        <li class="nav-menu__item">About Us</li>
        <li class="nav-menu__item">Blog</li> -->
    </ul>
</template>

<script>
export default {
  name: "Menu",
   //   el: "#menu",
    data: function() {
        return {
            items: ["Main", "Portfolio", "About Us", "Blog"]
        };
    }
}
</script>

<style scoped lang="scss">

// .nav-menu {
//     flex-grow: 1;
//     padding-left: 0;
//     display: flex;
//     justify-content: space-around;
//     align-items: center;
//     &__item {
//       list-style-type: none;
//       font-size: 23px;
//     }
//   }
</style>