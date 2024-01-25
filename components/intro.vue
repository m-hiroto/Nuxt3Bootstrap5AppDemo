<template>
    <div>
      <h1>{{ guitar.title }}</h1>
  
      <div class="row">
        <div class="col-4 left-side">
          <section class="introduction-section">
            <h2>自己紹介</h2>
            <p>
              こんにちは、私は[あなたの名前]と申します。ギターを愛し、その美しさや表現力に魅了されています。
              [他の自己紹介の内容を追加]
            </p>
          </section>
  
          <section class="experience-section">
            <h2>ギターの経歴</h2>
            <p>
              ギターを始めたのは[開始した年]年です。その後、[どのようなジャンルやバンドで演奏した経験]など、
              様々な経験を積んできました。[他の経歴の内容を追加]
            </p>
          </section>
  
          <section class="site-introduction-section">
            <h2>このサイトで紹介したいこと</h2>
            <p>
              このサイトでは、ギターに関する情報やアドバイス、お気に入りの楽曲のカバーなどを共有しています。
              ギター愛好者や初心者の方に役立つ情報を提供し、共にギターの素晴らしさを感じる場となればと思っています。
            </p>
          </section>
        </div>
        <div class="col-8 right-side">
          <p>画像</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  const guitar = useGuitar();
  </script>
  
  <style scoped>
  .introduction-section,
  .experience-section,
  .site-introduction-section {
    margin-bottom: 30px;
  }
  
  h2 {
    color: #333;
  }
  
  p {
    color: #666;
    line-height: 1.6;
  }
  
  .row {
    display: flex;
  }
  
  .left-side {
    flex: 1;
    padding: 20px;
  }
  
  .right-side {
    flex: 2;
    padding: 20px;
    background-color: #f5f5f5;
  }
  </style>
  