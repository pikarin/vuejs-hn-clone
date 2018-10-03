<template>
  <div class="pure-menu pure-menu-horizontal">
    <div class="container">
      <router-link :to="{ name: 'home' }" class="pure-menu-heading pure-menu-link">Home</router-link>
      <ul class="pure-menu-list">
        <li class="pure-menu-item">
          <router-link :to="{ name: 'new' }" class="pure-menu-link">New</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar"
};
</script>

<style lang="scss" scoped>
.pure-menu {
  background-color: #e17842;

  a {
    color: #ffffff;
  }
}
</style>
