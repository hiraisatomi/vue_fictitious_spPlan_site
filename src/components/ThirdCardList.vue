<script setup lang="ts">
import CardVue from './Card.vue'
import CardList from './CardList.vue';
import SecondCardListVue from './SecondCardList.vue';
</script>


<template>
<div class="container">
    <Card title="Title" class="card">
      <div class="contents">
        <h2 class="sub">ハイスペックプラン</h2>
        <p class="price">&yen;3,980(税込)/月</p>
        <div><img src="../assets/highspec.jpeg" alt="standard_plan_img"></div>
      </div>
    </Card>

    <Card title="Concept" class="card">
      <div class="contents">
        <h2 class="sub">特典付き&#033;とことんスマホライフを楽しみたい方へ</h2>
        <p>外でもガンガン使う&#033;せっかくなら他のサービスも利用したい&#033;</p>
        <p>そんな皆様にちょっとリッチで楽しいプランをご用意しました。</p>
      </div>
    </Card>

    <Card title="Plan" class="card with-text-card">
      <div class="contents plan">
        <h2 class="sub pcg">プラン内容</h2>
        <ul>
          <li>通信量&#058;〜30GB/月</li>
          <li>通話料&#058;かけ放題/月</li>
          <li>携帯故障サポート&#058;有り</li>
          <li><span class="special">特典1</span>&#058;mytube1ヶ月無料<br>(2ヶ月目以降&yen;780/月)</li>
          <li><span class="special">特典2</span>&#058;Just fit Pay&yen;5,000分<br>プレゼント</li>
        </ul>
      </div>
    </Card>
  </div>
</template>


<style scoped>
.container {
  max-width: 750px;
  display: flex;
  flex-direction: column;
  text-align: center;
  font-size: 13px;
}

.contents {
  margin: 0 auto;
  width: 100%;
}

.contents.plan {
  background-color: rgb(227, 227, 227);
  padding: 20px 0;
  border-radius: 8px;
}

.sub {
  font-size: 24px;
}

.sub.pcg {
  margin-top: 0;
}

.card {
  margin-bottom: 8px;
  display: flex;
}

.price {
  font-size: 18px;
  font-weight: bold;
}

.special {
  background-color: rgba(210, 208, 141, 0.7);
}

img {
  width: 100%;
  border-radius: 8px;
}

ul {
  margin: 0 auto;
  width: 155px;
  padding-left: 10px;
}

li {
  text-align: left;
}

</style>