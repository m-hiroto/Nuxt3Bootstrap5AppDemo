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
          name: "YAMAHA FS830",
          image: "https://m.media-amazon.com/images/I/71KtvGyNi2L.__AC_SX300_SY300_QL70_ML2_.jpg",
          link: "https://www.amazon.co.jp/%E3%83%A4%E3%83%9E%E3%83%8F-Yamaha-FS830-YAMAHA-%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC/dp/B01BDMKLL6/ref=sr_1_5?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&crid=2UPLD9SODO5GZ&keywords=FS830&qid=1707186914&sprefix=fs830%2Caps%2C158&sr=8-5&th=1",
          description: "YAMAHAのFシリーズのサイドバック材ローズモデル！",
          comments: "ヤマハのスモールボディギターの操作性の良さはもちろん、サイドとバックの素材がローズウッドで作られておりきらびやかな音鳴りが特徴で初心者にも扱いので最初のギターにお勧め！",
        }, 
        {
          name: "Epiphone Hummingbird",
          image: "https://m.media-amazon.com/images/I/51DJ1k9IL9S._AC_SY879_.jpg",
          link: "https://www.amazon.co.jp/Epiphone-Hummingbird-PRO-FC-%E3%82%A8%E3%83%AC%E3%82%AF%E3%83%88%E3%83%AA%E3%83%83%E3%82%AF%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC/dp/B00O0HUBI0/ref=sr_1_6?crid=2660535KOU2DE&keywords=%E3%83%8F%E3%83%9F%E3%83%B3%E3%82%B0%E3%83%90%E3%83%BC%E3%83%89+%E3%82%AE%E3%82%BF%E3%83%BC&qid=1706077632&sprefix=hamingu%2Caps%2C164&sr=8-6",
          description: "ハチドリがギター本体に描かれたおしゃれなギター！",
          comments: "操作性や低音の音鳴りの良さが特徴のギターで、更にハチドリの描かれたギターは思わず弾きたくなってしまう外観でギターをつづけることが楽しくなる初心者にお勧めのギターです！",
        },
        {
          name: "Martin LX1 Little Martin",
          image: "https://m.media-amazon.com/images/I/71NZUPrykwL._AC_SX679_.jpg",
          link: "https://www.amazon.co.jp/Martin-%E3%83%AA%E3%83%88%E3%83%AB%E3%83%9E%E3%83%BC%E3%83%81%E3%83%B3-%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC-LX-1-%E3%83%95%E3%82%A9%E3%83%BC%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC/dp/B01EQEPKUU/ref=sr_1_2?crid=OHGIAY0LZX6G&keywords=martin+%E3%83%9F%E3%83%8B%E3%82%AE%E3%82%BF%E3%83%BC&qid=1706077772&sprefix=martin+mi%2Caps%2C164&sr=8-2",
          description: "マーティンのミニエレクトリックアコースティックギター！",
          comments: "ミニギターならではの弾きやすさはそのままに、ミニギター特融のお隣の悪さのない初心者にお勧めのギターです!また、エレアコとしても使用できるので機材につないで使えるのもお勧めできるポイントです！",
        },
        {
          name: "Fender CC-60S Concert",
          image: "data:image/jpeg;base64,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",
          link: "https://www.amazon.co.jp/Fender-%E3%82%A2%E3%82%B3%E3%83%BC%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E3%82%AE%E3%82%BF%E3%83%BC-CC-60S-Concert-Natural/dp/B07FYW9M4Q/ref=sr_1_5?__mk_ja_JP=%E3%82%AB%E3%82%BF%E3%82%AB%E3%83%8A&crid=N6D29UCBPSVI&keywords=fender%2B%E3%82%A2%E3%82%B3%E3%82%AE&qid=1706590882&sprefix=fender%2B%E9%98%BF%E6%BC%95%2Caps%2C157&sr=8-5&th=1",
          description: "エレキギターメーカーが作るアコースティックギター！",
          comments: "エレキギターが作るギター特融のネックの薄さによる弾きやすさとボディ形状による音のバランスがとても良いギターです！音と弾きやすさのバランスが良く自分に合ったギターを見つけるのが難しい初心者にお勧めのギターです！",
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
  flex: 0.3;
  max-height: 220px; /* 4行に合わせた適切な高さ */
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
