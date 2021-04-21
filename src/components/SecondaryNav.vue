<template>
  <el-menu
    :default-active="activeIndex"
    mode="horizontal"
    background-color="white"
    active-text-color="black"
  >
    <el-menu-item @click="drawer = true" index="1">All</el-menu-item>
        <el-drawer v-model="drawer" direction="ltr" title="Welcome!" size="20%">
          <p class="drawer-item" v-for="category in categories" :key="category">{{category}}</p>
        </el-drawer>
    <el-menu-item index="2">Bestsellers</el-menu-item>
    <el-menu-item index="3">New</el-menu-item>
    <el-menu-item index="4">Electronics</el-menu-item>
    <el-menu-item index="5">Home</el-menu-item>
    <el-menu-item index="6">Fashion</el-menu-item>
    <el-menu-item index="7">Grocery</el-menu-item>
    <el-menu-item index="8">Health</el-menu-item>
    <el-menu-item index="9">Exclusive</el-menu-item>
    <el-menu-item index="10">Gifts</el-menu-item>
    <el-menu-item index="11">Coupons</el-menu-item>
  </el-menu>
</template>

<script>
export default {
  name: "SecondaryNav",
  data() {
      return {
          drawer: false,
          categories: [
            "Trending",
            "Bestsellers",
            "New Releases",
            "Electronics",
            "Home",
            "Fashion",
            "Grocery",
            "Health"
          ]
      }
  }
};
</script>

<style scoped>
.el-menu {
  display: flex;
  align-items: center;
  justify-content: center;
}
.el-menu-item {
  color: rgb(94, 94, 94);
}
.el-button {
  size: small;
  background-color: rgb(0, 31, 131);
  color: white;
}
.drawer-item {
  color: rgb(94, 94, 94);
  margin-left: 50px;
}

</style>