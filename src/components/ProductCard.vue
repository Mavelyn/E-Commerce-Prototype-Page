<template>
  <el-row>
    <el-col>
      <el-card :body-style="{ padding: '0px'}" shadow="never">
        <img :src="product.image_url" class="image" />
        <div style="padding: 15px">
          <span>{{ product.name }}</span>
          <span>
            <Rating :rating="product.rating"/>
          </span>
          <span style="padding: 5px">${{product.price}}</span>
        </div>
      </el-card>
    </el-col>
  </el-row>
</template>

<script>
import Rating from './Rating.vue'

export default {
  props: ["product"],
  components: {
      Rating
  }
};
</script>

<style scoped>
.bottom {
  display: flex;
  justify-content: center;
  align-items: center;
}

.image {
  width: 300px;
  height: 200px;
  display: block;
  object-fit: cover;
}
.el-col {
  padding: 10px;
}
.el-button {
    padding: 10px;
    margin-bottom: 20px;
}
</style>