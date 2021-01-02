<template>
  <nav class="nav">
    <img src="../../assets/logo.png" alt="Logo Company" class="logo" />
    <!-- <ul class="nav-menu">
        <li class="nav-menu__item">Head</li>
        <li class="nav-menu__item">Portfolio</li>
        <li class="nav-menu__item">About Us</li>
        <li class="nav-menu__item">Blog</li>
    </ul> -->
    <Menu/>
  </nav>
</template>

<script>
import Menu from "../header/Menu.vue";
export default {
  name: 'Header',
  components: {
      Menu
  }
  
};
</script>

<style lang="scss">
.logo {
  width: 100px;
  height: 100px;
}
.nav {
  display: flex;
  &-menu {
    flex-grow: 1;
    padding-left: 0;
    display: flex;
    justify-content: space-around;
    align-items: center;
    &__item {
        list-style-type: none;
        font-size: 23px;
    }
  }
}
</style>