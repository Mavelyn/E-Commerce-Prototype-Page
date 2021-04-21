<template>
  <el-input placeholder="Search" v-model="input" class="search_bar">
    <template #prepend>
      <el-select placeholder="Select" v-model="select" class="input-with-select">
        <el-option
          v-for="item in options"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        >
        </el-option>
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
  // data() {
  //   return {
  //   };
  // },
  setup() {
    return {
      
      options: [
        {
          value: "1",
          label: "All",
        },
        {
          value: "2",
          label: "Bestsellers",
        },
        {
          value: "3",
          label: "New",
        },
        {
          value: "4",
          label: "Electronics",
        },
        {
          value: "5",
          label: "Home",
        },
        {
          value: "6",
          label: "Fashion",
        },
        {
          value: "7",
          label: "Grocery",
        },
        {
          value: "8",
          label: "Health",
        }
      ],
      input: ref(''),
      select: ref(''),
    };
  },
});
</script>

<style scoped>
.search_bar {
  align-self: center;
  flex-grow: 2;
}
.input-with-select {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>