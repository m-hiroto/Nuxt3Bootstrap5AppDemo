<template>
<div>
   <div class="title offset-1">
    <h1>{{ guitar.title }}</h1>
   </div>
    <div class="row">
     
      <div class="col-11 offset-1 left-side">
        <section class="introduction-section">
          <h2>    自己紹介</h2>
          <p>    初めまして前野洋斗といいます。このサイトを書いている主です。<br>現在19歳でこの学校ではロボット専攻に所属しています.</p>
        </section>

        <section class="experience-section">
          <h2>    ギター歴</h2>
          <p>    ギターを始めたのは今から３年前で主にアコースティックギターを弾いてきました。<br>様々な演奏法がある中で弾き語りを中心にギターを演奏してきました.</p>
        </section>

        <section class="site-introduction-section">
          <h2>    このサイトで紹介したいこと</h2>
          <p>    このサイトでは、アコースティックギターを購入しようとしている人に向けた個人的なお勧めギターを紹介しています。<br>このサイトをきっかけにギターに興味を持ってくれる人がいたら嬉しいです！</p>
        </section>
      </div>

      <div class="col-1 offset-4 right-side">
        <!-- 通常のimgタグを使用 -->
        <img src="images/IMG_6346.JPG" alt="Guitar Image" class="image-size" />
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
  font-size: large;
   
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
  max-width: 1000px;
  
}

.image-size {
  width: 500px; /* 画像の幅を親要素に合わせる */
  
  
}
</style>
