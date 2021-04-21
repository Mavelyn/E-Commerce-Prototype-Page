<template>
  <el-input placeholder="Search" v-model="input" class="search_bar">
    <template #prepend>
      <el-select placeholder="All" v-model="select" class="input-with-select">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        >
        </el-option>
        <!-- <el-option label="Electronics" value="1"></el-option> -->
      </el-select>
    </template>
    <template #append>
      <el-button icon="el-icon-search"></el-button>
    </template>
  </el-input>
</template>

<script>
import { defineComponent, ref } from "vue";
export default defineComponent({
  data() {
    return {
      options: [
        {
          value: "All",
          label: "All",
        },
        {
          value: "Bestsellers",
          label: "Bestsellers",
        },
        {
          value: "New",
          label: "New",
        },
        {
          value: "Electronics",
          label: "Electronics",
        },
        {
          value: "Home",
          label: "Home",
        },
        {
          value: "Fashion",
          label: "Fashion",
        },
        {
          value: "Grocery",
          label: "Grocery",
        },
        {
          value: "Health",
          label: "Health",
        }
      ],
    };
  },
  setup() {
    return {
      input: ref(""),
      select: ref(""),
    };
  },
});
</script>

<style scoped>
.search_bar {
  align-self: center;
  flex-grow: 2;
}
</style>