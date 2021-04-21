<template>
    <el-row class="navbar">
            <el-col :span="4" class="el-menu el-menu--horizontal navbar_logo">
                <li>MARKET</li>
            </el-col>
            <el-col :span="20">
                <ul class="el-menu el-menu--horizontal navbar">
                    <SearchBar/>
                    <li class="el-menu-item">Orders</li>
                    <li class="el-menu-item"><el-avatar src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png"></el-avatar></li>
                    <li class="el-menu-item"><i class="el-icon-shopping-cart-2"></i></li>
                </ul>
            </el-col>
        </el-row>
</template>

<script>
import SearchBar from './SearchBar.vue'
export default {
    name: 'NavBar',
    components: {
        SearchBar
    }
}
</script>

<style scoped>
.navbar {
    flex: 1;
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    align-content: center;
    background-color: white;
    margin: 0;
    padding: 0;
}
.navbar_logo {
    background-color: white;
    list-style: none;
    color: black;
    display: flex;
    font-weight: bold;
    font-size: 24px;
    align-items: center;
    padding-left: 120px;
}

.el-menu-item {
    color: black;
}
</style>