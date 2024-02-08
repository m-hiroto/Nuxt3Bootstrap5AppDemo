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
        <p v-if="product.comments" v-html="product.comments"></p>
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
          name: "HONEY BEE F-15",
          image: "https://m.media-amazon.com/images/I/51sRXkPdxWL._AC_UF894,1000_QL80_.jpg",
          link: "https://www.amazon.co.jp/HONEY-BEE-%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC-%E3%83%95%E3%82%A9%E3%83%BC%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC%E3%82%BF%E3%82%A4%E3%83%97-F-15/dp/B0086TF8R2",
          description: "一万円台ならこのギター！！",
          comments: "一万円台で購入できるギターの中ではトップクラスの引きやすさと音の良さで特にバランスが優秀なギターです！<br>さらに初心者セットも販売されているのでとにかく安く始めたいという人にもおすすめ！",
        },
        {
          name: "YAMAHA FS820",
          image: "https://m.media-amazon.com/images/I/61XycEyHQyL._AC_SX679_.jpg",
          link: "https://www.amazon.co.jp/%E3%83%A4%E3%83%9E%E3%83%8F-YAMAHA-%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC-%E3%83%8A%E3%83%81%E3%83%A5%E3%83%A9%E3%83%AB-FS820/dp/B08QZ1GHJR/ref=sr_1_3?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&crid=7Z1A90E7JE4Y&keywords=yamaha%2Bfs820&qid=1705956144&s=musical-instruments&sprefix=yamaha%2Bfs820%2Cmi%2C208&sr=1-3&th=1",
          description: "三万円台ならこのギター！！",
          comments: "YAMAHAのシリーズのスモールボディ機種！<br>スモールボディならではの操作性の高さ！<br>この価格ではトップクラスの性能、操作性でTOP材が単板ということもありこの価格帯では破格のコストパフォーマンスと音鳴りの良さです！"
        },
        {
          name: "YAMAHA LS6",
          image: "https://m.media-amazon.com/images/I/61IH7HjPO4L._AC_SX679_.jpg",
          link: "https://www.amazon.co.jp/%E3%83%A4%E3%83%9E%E3%83%8F-%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC-LL6-ARE-%E3%83%91%E3%83%83%E3%82%B7%E3%83%96%E3%82%BF%E3%82%A4%E3%83%97%E3%83%94%E3%83%83%E3%82%AF%E3%82%A2%E3%83%83%E3%83%97%E6%90%AD%E8%BC%89/dp/B00IHW3UIM/ref=sr_1_1_sspa?crid=5HW1ELYRCOR2&keywords=yamaha%2Bls6&qid=1705956479&s=musical-instruments&sprefix=yamaha%2Bls%2Cmi%2C260&sr=1-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&th=1",
          description: "五万円台ならこのギター！！",
          comments: "YAMAHAのLシリーズの中の<br>スモールボディ機種！<br>スモールボディならではのきらきらとした音が特徴のギターです！<br>またこの価格でエレアコとしても使用でき、低音域もしっかりと鳴らすことができる素晴らしい機種です！",
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
  flex: 0.3;
  max-height: 300px; /* 3行に合わせた適切な高さ */
  overflow: auto; /* コンテンツが高さを超える場合はスクロールバーを表示 */
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
  font-weight: 900;
  line-height:200%
}




</style>