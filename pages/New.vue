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
          name: "YAMAHA FG820",
          image: "https://m.media-amazon.com/images/I/51jjpLHJU8L._AC_SY879_.jpg",
          link: "https://www.amazon.co.jp/%E3%83%A4%E3%83%9E%E3%83%8F-YAMAHA-FG820-%E8%A3%8F%E3%83%BB%E5%81%B4%E6%9D%BF%E3%81%AB%E3%83%9E%E3%83%9B%E3%82%AC%E3%83%8B%E3%83%BC%E3%82%92%E6%8E%A1%E7%94%A8-%E3%81%82%E3%81%9F%E3%81%9F%E3%81%8B%E3%81%BF%E3%81%AE%E3%81%82%E3%82%8B%E3%83%91%E3%83%AF%E3%83%95%E3%83%AB%E3%81%AA%E3%82%B5%E3%82%A6%E3%83%B3%E3%83%89%E3%81%A8%E8%B1%8A%E5%AF%8C%E3%81%AA%E3%82%AB%E3%83%A9%E3%83%BC%E3%83%90%E3%83%AA%E3%82%A8%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%8C%E9%AD%85%E5%8A%9B/dp/B08QV61DB7/ref=sr_1_5?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&crid=2PH1MVGL9JE5C&keywords=fg820&qid=1706077445&sprefix=fg820%2Caps%2C157&sr=8-5",
          description: "商品1の説明や詳細情報などがここに入ります。",
          comments: "商品1のコメントやレビューなどの情報が入ります。",
        }, 
        {
          name: "Epiphone Hummingbird",
          image: "https://m.media-amazon.com/images/I/51DJ1k9IL9S._AC_SY879_.jpg",
          link: "https://www.amazon.co.jp/Epiphone-Hummingbird-PRO-FC-%E3%82%A8%E3%83%AC%E3%82%AF%E3%83%88%E3%83%AA%E3%83%83%E3%82%AF%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC/dp/B00O0HUBI0/ref=sr_1_6?crid=2660535KOU2DE&keywords=%E3%83%8F%E3%83%9F%E3%83%B3%E3%82%B0%E3%83%90%E3%83%BC%E3%83%89+%E3%82%AE%E3%82%BF%E3%83%BC&qid=1706077632&sprefix=hamingu%2Caps%2C164&sr=8-6",
          description: "商品2の説明や詳細情報などがここに入ります。",
          comments: "商品2のコメントやレビューなどの情報が入ります。",
        },
        {
          name: "Martin LX1 Little Martin",
          image: "https://m.media-amazon.com/images/I/71NZUPrykwL._AC_SX679_.jpg",
          link: "https://www.amazon.co.jp/Martin-%E3%83%AA%E3%83%88%E3%83%AB%E3%83%9E%E3%83%BC%E3%83%81%E3%83%B3-%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC-LX-1-%E3%83%95%E3%82%A9%E3%83%BC%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC/dp/B01EQEPKUU/ref=sr_1_2?crid=OHGIAY0LZX6G&keywords=martin+%E3%83%9F%E3%83%8B%E3%82%AE%E3%82%BF%E3%83%BC&qid=1706077772&sprefix=martin+mi%2Caps%2C164&sr=8-2",
          description: "商品3の説明や詳細情報などがここに入ります。",
          comments: "商品3のコメントやレビューなどの情報が入ります。",
        },
        {
          name: "Morris  Perfomers Edition F-011 NAT",
          image: "https://m.media-amazon.com/images/I/31Cre7GJB0L._AC_US40_.jpg",
          link: "https://www.amazon.co.jp/Morris-MORRIS-F-011-NAT-%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC/dp/B08R9PWJXV/ref=sr_1_3?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&crid=3Q22QY7BYS6YT&keywords=%E3%83%A2%E3%83%BC%E3%83%AA%E3%82%B9%2B%E3%82%A2%E3%82%B3%E3%82%AE&qid=1706077964&sprefix=%E3%83%A2%E3%83%BC%E3%83%AA%E3%82%B9%E3%82%A2%E3%82%B3%E3%82%AE%2Caps%2C161&sr=8-3&th=1",
          description: "商品4の説明や詳細情報などがここに入ります。",
          comments: "商品4のコメントやレビューなどの情報が入ります。",
        },
        {
          name: "YAMAHA LS6 ARE",
          image: "https://m.media-amazon.com/images/I/61NNzFwlNmL._AC_SX679_.jpg",
          link: "https://www.amazon.co.jp/%E3%83%A4%E3%83%9E%E3%83%8F-YAMAHA-%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC-LS6-ARE/dp/B00IHW3VFE/ref=sr_1_3?crid=118FVG7U6N1KJ&keywords=ls6%2Bare&qid=1706078087&sprefix=ls6%2Caps%2C164&sr=8-3&th=1",
          description: "商品5の説明や詳細情報などがここに入ります。",
          comments: "商品5のコメントやレビューなどの情報が入ります。",
        },
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
  height: 300px;
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
