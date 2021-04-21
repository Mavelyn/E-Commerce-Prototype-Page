<template>
    <el-row>
        <el-col>
            <p>Brand</p>
            <el-checkbox-group v-model="checkList1">
                <div v-for="option in options1" :key="option.value">
                    <el-checkbox :label="option.label"></el-checkbox>
                </div>
                <el-divider></el-divider>
            </el-checkbox-group>
            <p>Categories</p>
            <el-checkbox-group v-model="checkList2">
                <div v-for="option in options2" :key="option.value">
                    <el-checkbox :label="option.label"></el-checkbox>
                </div>
                <el-divider></el-divider>
            </el-checkbox-group>
            <p>Current Offers</p>
            <el-checkbox-group v-model="checkList3">
                <div v-for="option in options3" :key="option.value">
                    <el-checkbox :label="option.label"></el-checkbox>
                </div>
                <el-divider></el-divider>
            </el-checkbox-group>
        </el-col>
    </el-row>
</template>

<script>
export default {
    data() {
        return {
            checkList1:[],
            checkList2:[],
            checkList3:[],
            options1: [
                {
                    label: "Apple",
                    value: "Apple"
                },
                {
                    label: "Microsoft",
                    value: "Microsoft"
                },
                {
                    label: "LG",
                    value: "LG"
                },
                {
                    label: "Lenovo",
                    value: "Lenovo"
                }
            ],
            options2: [
                {
                    label: "Laptops",
                    value: "Laptops"
                },
                {
                    label: "Chromebooks",
                    value: "Chromebooks"
                },
                {
                    label: "Gaming Laptops",
                    value: "Gaming Laptops"
                },
                {
                    label: "Touchscreen",
                    value: "Touchscreen"
                }
            ],
            options3: [
                {
                    label: "On Sale",
                    value: "On Sale"
                },
                {
                    label: "Top Deals",
                    value: "Top Deals"
                },
                {
                    label: "On Clearance",
                    value: "On Clearance"
                },
                {
                    label: "Exclusive",
                    value: "Exclusive"
                }
            ]
        }
    }
}
</script>

<style scoped>
.el-col {
  padding-left: 100px;
  margin-top: 40px;
}
.el-checkbox-group {
    justify-self: flex-start;
}
</style>