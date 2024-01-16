<template>
  <div class="container">
    <div v-for="(product, index) in products" :key="index" class="product">
      <div class="left-side">
        <img :src="product.image" alt="Product Image">
        <h2><a :href="product.link" target="_blank">{{ product.name }}</a></h2>
        <p>{{ product.description }}</p>
      </div>
      <div class="right-side">
        <h2>コメント</h2>
        <p>{{ product.comments }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          name: "商品1",
          image: "商品1の画像のURL",
          link: "商品1のリンクのURL",
          description: "商品1の説明や詳細情報などがここに入ります。",
          comments: "商品1のコメントやレビューなどの情報が入ります。",
        },
        {
          name: "商品2",
          image: "商品2の画像のURL",
          link: "商品2のリンクのURL",
          description: "商品2の説明や詳細情報などがここに入ります。",
          comments: "商品2のコメントやレビューなどの情報が入ります。",
        },
        // 他の商品データも追加できます
      ],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: flex-start;
}

.product {
  display: flex;
  width: 100%;
  margin-bottom: 20px;
}

.left-side {
  flex: 1;
  padding: 20px;
}

.right-side {
  flex: 1;
  padding: 20px;
  background-color: #f5f5f5;
}

img {
  max-width: 100%;
  height: auto;
  border-radius: 5px;
  margin-bottom: 10px;
}

a {
  color: #007bff;
  text-decoration: none;
}

h2 {
  color: #333;
}

p {
  color: #666;
}
</style>